---
layout: post
title:  "Uploader for Sinatra Portfolio Project"
date:   2017-01-12 20:35:33 +0000
---

Simply put, I wanted to build a web app that would upload images and display them.

When I began my Sinatra project I was inspired by [Instagram](https://www.instagram.com/).  I don't have an Instagram account but I am captured by photos.  I viewed a few previous Sinatra projects from students who implemented an upload function and decided to try the simple [Ruby File class](http://ruby-doc.org/core-2.2.0/File.html).  I read up on a few students blog posts also to gain understanding on how this file upload function would work.

## Ruby File class
Foremost, Ruby has a good, old file class that allows you to write files to a disk.  The file class I used in my project includes an [enctype attribute](https://www.w3.org/TR/html401/interact/forms.html#h-17.3) that specifies the [content type](https://www.w3.org/TR/html401/interact/forms.html#form-content-type).  Content type is neccesary if the form submission includes files.  Enctype has three different values but the value I needed to use was `multipart/form-data` which should be used in combination with the input element type equal to `"file"`.

With further research I learned that [enctype](http://www.w3schools.com/tags/att_form_enctype.asp) allows files to be sent through a POST route that does not encode characters.  This function is useful while uploading files to a server that requires binary data to be uploaded.

## Upload Form
My Finstagram app included two upload actions.  I had a User and Post object.  With my User, I built the `edit.erb` view to include a form for uploading a photo file from your computer.  With my Post, I built the `new.erb` view.

This upload function was then executed in my `UserController PATCH action` and `PostController POST action` by retrieving and opening the file then writing the file to the disk for completion.  Once the upload was successful the photo would be saved in the routed public directory.

## Responsibility
In a few examples I browsed, the upload function was responsible for retrieving, opening, writing and saving the files in its own controller.  This was plausible but in my case I wanted to maintain the ownership of each file uploaded.  If I created a new post with a photo and a caption, I wanted that uploaded file to be under the responsibility of the Post.  The same goes with the User.  With this maintenance, I was able to establish organization while building my app.

User photo form	
```
<h1>Edit your Profile</h1>
<form action="/users/<%= @user.id %>" method="post" enctype="multipart/form-data">
  <input type="hidden" name="_method" value="patch">
  <label>Profile Photo </label>
  <input type="file" name="file" value="<%= @user.user_photo %>" required>
  <br><br>

  <input type="submit" value="Update Profile">
</form>
```

User photo action to handle file submission
```
  patch '/users/:id' do
    @user = User.find_by_id(params[:id])
    if params[:file]
      @filename = params[:file][:filename]
      file = params[:file][:tempfile]
      File.open("./public/images/profile/#{@filename}", 'wb') do |f|
        f.write(file.read)
      end
      @user.update(user_photo: @filename)
      flash[:success] = "Profile successfully updated!"
      redirect "/users/#{@user.id}"
    else
      flash[:error] = "Your profile did not update correctly"
      redirect "/users/#{@user.id}/edit"
    end
  end
	```

Post Form
```
<h1>Create a new post</h1>
<form action="/posts" method="post" enctype="multipart/form-data">
  <label>Photo of Post :</label>
  <input type="file" name="file" value="">
  <br><br>

  <label>Caption: </label>
  <input type="text" name="caption" value="">
  <br><br>

  <input type="submit" name="" value="Create Post">
</form>
```

Post action to handle file submitssion
```
  post '/posts' do
    if params[:file] && params[:caption] != ""
      @post = Post.create(caption: params[:caption], user_id: session[:user_id])
      @filename = params[:file][:filename]
      file = params[:file][:tempfile]
      File.open("./public/images/post/#{@filename}", 'wb') do |f|
        f.write(file.read)
      end
      @post.post_photo = @filename
      @post.save
      flash[:success] = "Post successfully made!"
      redirect '/posts'
    else
      flash[:error] = "Please make sure both fields are present."
      redirect '/posts/new'
    end
  end
	```
	
	
