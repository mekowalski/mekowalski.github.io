---
layout: post
title:  "The RESTful Seven"
date:   2017-02-07 19:52:40 +0000
---


Roy T. Fielding wasn't digging the style of the URL's presence back in the day.  He decided there needed to be a better convention.  RESTful actions came into play as an architetural styling of URLs, a standard naming convention for mapping URLs and their corresponding controller actions. With these RESTful actions there maintained consistent properties and gave a certain feel to them.

## INDEX action
The INDEX action displays a collection of resources.  Generally this basic action will view an associated template about each resource.  For each resource a link is attached to gain detailed information regarding that specific resource.  The most simple example of the INDEX action will be:

```
  def index
    @dogs = Dog.all
  end
```
## SHOW action
SHOW action is responsible for displaying information on one object of the collection.  With the dog example from above, I should be able to click the attached link of a dog and be directed to details regarding that one dog.  An example of the SHOW action is:

```
  def show
    @dog = Dog.find(params[:id])
  end
```
## DESTROY action
The DESTROY action is quite self explanatory.  This action deletes a specific resource in the collection.  An example of the DESTROY action is:

```
  def destroy
    @dog = Dog.find(params[:id])
	  redirect_to dogs_path
  end
```
## NEW action
The task of the NEW action is simply to display a form to produce a new entity that is waiting to be made.  A simple NEW action will be:

```
  def new
    @dog = Dog.new
  end
```
## CREATE action
The NEW action is the first step in a new object being made.  The second step is the CREATE action.  CREATE actually goes forward to make the new entity occur based on input.  This action will save and build the entity successfully with a following of displaying the new resource.  If by some means the object failes to save and be built CREATE will then render NEW to try again.  NEW and CREATE work together.  An example of CREATE action is:

```
  def create
    @dog = Dog.new(dog_params)
    if @dog.save
      redirect_to dog+path(@dog)
    else
      render :new
    end
  end
```
## EDIT action
The task of EDIT action is simple also that if provides a form to modify a resource.  A simple EDIT action is:

```
  def edit
	@dog = Dog.find(params[:id])
  end
```
## UPDATE action
Similar to the relationship of NEW and CREATE, EDIT works with UPDATE to process the form with the input recieved and displays the view of the modified resource.  UPDATE will also render EDIT to try again if the inital modification failed to be updated.  An example of UPDATE action will be:

```
  def update
    if @dog.update(dog_params)
      redirect_to dog_path(@dog)
    else
      render :edit
    end
  end
```

## A word in private please?
In the CREATE and UPDATE actions I am taking in an argument of `dog_params` that is built in a prviate method.  This is included in the controller and used in an action that may need the params of an object.  An example of this private method may look like this:

```
  private
	
  def dog_params
    params.require(:dog).permit(:name, :age, :breed)
  end
```
