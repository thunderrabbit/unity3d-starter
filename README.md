# Initial Unity3D project

### [using git for Unity3D](http://stackoverflow.com/a/18225479/194309)

1. Create a project with Unity
2. Edit → Project Settings → Editor → Version Control Mode: Visible Meta Files
3. Edit → Project Settings → Editor → Asset Serialization Mode: Force Text

````
    cd ~/path/to/unity/project/
	
    git clone https://github.com/thunderrabbit/unity3d-starter.git  tmp
    cp tmp/.gitignore .
    echo "my great project" >> README.md
    rm -rf tmp
    git init
````


### New to git?  Here's what's happening:

Go to the directory where you saved the project.

````
    cd ~/path/to/unity/project/
````

In this directory, you should see something like the following if you `ls`:

````
drwxr-xr-x   4 thunderrabbit  staff  136 Apr  7 16:22 Assets
drwxr-xr-x  20 thunderrabbit  staff  680 Apr  7 16:22 Library
drwxr-xr-x  16 thunderrabbit  staff  544 Apr  7 16:22 ProjectSettings
drwxr-xr-x   4 thunderrabbit  staff  136 Apr  7 16:22 Temp
````

Next, we're 'cloning' this git repository, primarily because we're interested in the `.gitignore` file.  We put it in the `tmp` directory because we're not going to keep the repo.

`.gitignore` is a file that tells git what files to ignore.  There are lots of files Unity creates which can be recreated in a trice.  There's no reason for them to clutter your repository.

````
    git clone https://github.com/thunderrabbit/unity3d-starter.git  tmp
````

Okay copy the `.gitignore` file to your Unity project.

````
    cp tmp/.gitignore .
````

Now create a `README.md` file for your project.  (actually the >> means to append to the file so it won't get clobbered in case it already exists.)

````
    echo "my great project" >> README.md
````

Now wipe the `tmp` directory because we don't need it.

````
    rm -rf tmp
````

Now, initialize your git repository.

````
    git init
````

Now we'll tell git to remember the initial state of the project.

````
    git add .
````

And finally commit the changes:

````
    git commit -m "First commit in my project wowzers"
````
