# Proj

![Proj Screenshot]
(proj-screenshot.png)

## A command line tool for switching codebases, projects, and context. 

### Primer:

As a developer, you'll often find yourself constantly switching between codebases. Proj offers a simple and intuitive command line application for quickly starting, and tearing down code projects. 

### Install

Ensure you have Go on your local system. 

1. git clone https://github.com/EwanValentine/proj
2. cd proj
3. go build && go install

### Use

#### Create a new proj project

Say you have a project in `/Users/ewanvalentine/Development/project-a`. 

Simply run... `proj init --name="project-a" --path="/Users/ewanvalentine/Development/project-a" --command="npm install && npm start"`. 

This will save a copy of your project, into a database, and it will create a `proj.yml` config file in your project root. You can alter your settings, by altering this yaml file, then runnning `proj commit` whilst in that directory. 

#### Start a project
Run `$ proj start my-project`

#### Stop a project
Run `$ proj stop my-project` - this will run your tear down script.

#### Todo:

- Add a current project state. Keeps track of the current running project.
- Add a 'teardown' command, for pulling a current project down, once a new project is started.
- Add commands as an array, rather than a single string. Ideally support both. 
- Support relative directories.
