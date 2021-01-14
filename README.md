# Todo CLI application

-use cases, running  application => commands(figure out requirements and usage of our application)

-structuring the code, how we will implement it
=> where to store the data
=> how to manipulate the data

-Implementation along with testing
-Run and use it :)

# Use cases 
- create a todo list
- show all the todo lists
- add, edit, delete, mark as complete, incomplete etc
  as todo items present in those lists
- show all the todo items in a perticular list

# Commands to use the CLI application

=> prefixes for the commands: list, todo
  lists = ['course1','course2','course3']
  'course1' => todos['read topic A','attempt test X',etc]

  list = collection of todos
  
- list show => show all the todo list we have
- list create list_name => create a list with 'list_name'
- list use list_name => select a perticular todo list

  todo is basically a task to be done e.g. learn loops in python,
  e.g. watch the previous lecture again
  
- todo add todo_title => add a todo item in the list
- todo all => show all todos in the selected list(give us id and title)
- todo edit item_id new_title => edit the item with id = item_id
- todo remove item_id => remove the item with id = item_id
- todo complete item_id =>marks the todo item with item_id as complete
- todo incomplete item_id => mark the todo item with item_id as incompletec

- help => print all the commands we can use in the application
- quit => Exit the application 

### lists.json
- stores a list of todo lists

[
	'list1';
	'list2'
]

check wheather a given list exists
=> using the above approach, need to iterate over all list elements

- store it as dict of todo list (dict => title and created_at)

data = {
  'list1':{
     'file_name': 'list1.json',
	 'created_at': time
  }
}

data['list1'][created_at]

=> checking if a list exists: title key exists or not?

### list1.json

- list of todo items
[
	{
		'title':'name1',
		'created_at': time,
		'completed': false
	},
	{
		'title':'name2',
		'created_at': time,
		'completed': false
	}
]

- serialize and deserialize the data