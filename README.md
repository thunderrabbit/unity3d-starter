# Initial Unity3D project

### [using git for Unity3D](http://stackoverflow.com/a/18225479/194309)

1. Create a project with Unity
2. Edit → Project Settings → Editor → Version Control Mode: Visible Meta Files
3. Edit → Project Settings → Editor → Asset Serialization Mode: Force Text

````
    cd ~/path/to/unity/project/
	
    git clone https://github.com/thunderrabbit/unity3d-starter.git  tmp
    cp tmp/.gitignore tmp/README.md .
    rm -rf tmp
    git init
````