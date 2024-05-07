# Initiation to C#

## Introduction

The `C#` language is an object-oriented programming language developed by Microsoft as part of its .NET platform. Introduced in 2000, `C#` swiftly rose to prominence as one of the most popular languages for application development, spanning desktop, web, and mobile applications.

It was crafted to be straightforward to learn and use, boasting a clear and intuitive syntax. 

What further contributes to its popularity is its extensive ecosystem of tools, libraries, and frameworks, facilitating the development of solutions with great ease.


## Installation

To develop in `C#`, you can use .NET Core, Microsoft's cross-platform framework for application development.
Here are the steps to install .NET Core on Fedora, here we will use the `3.1 SDK verison`:

```bash
sudo dnf install dotnet-sdk-3.1
```

> 💡 Verify if .NET Core is installed correctly : `dotnet --version`

## Part 0

`C#`, like `C++`, is an object-oriented language.
So to develop programs in this language, it is important to understand the basics of object-oriented.

Before beginning the exercise, it is important that you answer the following questions:
- What is an object-oriented language.
- What is a Class.
- What is a Constructor.
- What is a Modifier (public, private).

> 💡 Do not hesitate to ask questions if you have difficulties understanding notions

# Part 1

### Step 1

To get started, create your first `MyFirstApp` console application using dotnet.

```txt
B0-HUB-C# $> tree MyFirstApp/
MyFirstApp/
├── MyFirstApp.csproj
├── obj
│   ├── MyFirstApp.csproj.nuget.dgspec.json
│   ├── MyFirstApp.csproj.nuget.g.props
│   ├── MyFirstApp.csproj.nuget.g.targets
│   ├── project.assets.json
│   └── project.nuget.cache
└── Program.cs

2 directories, 7 files
```

### Step 2

"Now that the structure of your solution has been created, run your program and see what happens."

> Use `dotnet run` to run the program

### Step 3

Create a file `Human.cs` that contain an `Human` class.

When a `Human` object is created, it should simply display the following sentence in the console: `Hello!`.

### Step 4

Now, create an object of your `Human` class.
Your program should display something like this:

```txt
B0-HUB-C# $> dotnet run | echo $?
Hello!$
```

### Step 5

Alright, so far, nothing too complicated.
It would be better to have some information about the humans we create though.

In your `Human` class, add two attributes: `name` and `age`.

Modify the constructor of your class so that it can take the name and age of the created human as parameters.

Now, change the sentence displayed when an object of the Human class is created to: `[<name>]: Hello!`

> ⚠️ Warnings have appeared? Fix them!

### Step 6

Now, create an human who's name `Loic` and has 21 years old.
Your program should display something like this:

```txt
B0-HUB-C# $> dotnet run
[Loic]: Hello!
```

### Step 7

Greate, now we have infomations about our humans.
However, when a human is born by default, they are supposed to be 0 years old.
Change the constructor so that when creating a human, if the age is not specified, it is automatically set to `0`.

Then create a public function `howOldAreYou` that display the following sentece: `[<name>]: I am <age> years old`.

### Step 8

Now, create an other human who's name `Romain` without specify the age.
Then call the `howOldAreYou` function of the two object.
Your program should display something like this:

```txt
B0-HUB-C# $> dotnet run
[Loic]: Hello!
[Romain]: Hello!
[Loic]: I am 21 years old.
[Romain]: I am 0 years old.
```

### Step 9

Oops, there was a mistake in the prompt. Loic is actually 19 years old, not 21. Please update Loic's age and call the `howOldAreYou` function again.

```txt
B0-HUB-C# $> dotnet run
[Loic]: Hello!
[Romain]: Hello!
[Loic]: I am 21 years old.
[Romain]: I am 0 years old.
[Loic]: I am 19 years old.
```

### Step 10

Now, to develop the social skills of our humans, it would be nice if they could talk to each other.

Create a `talkWith` function that takes another `Human` object as a parameter and displays:

```txt
Start dialogue between <name> and <name2>.
[<name>]: Hello <name2>!
[<name2>]: Hello <name>!
[<name>]: How are you?
[<name2>]: I am fine, thank you!
[<name>]: Goodbye!
[<name2>]: Goodbye!
End dialogue between <name> and <name2>.
```

The `talkWith` function can also take no parameters. In that case, the function will display:

```txt
[<name>]: Hello ... Is there anyone?
[<name>]: I'm speaking alone ...
```


> ⚠️ No parameters provided, means **NO PARAMETERS**, so assigning default values is not allowed.

### Step 11

Now create a talk between Loic and Paul.
Then create a talk between Paul.

Your program should display something like this:

```txt
B0-HUB-C# $> dotnet run
[Loic]: Hello!
[Paul]: Hello!
[Loic]: I am 21 years old.
[Paul]: I am 0 years old.
[Loic]: I am 19 years old.
Start dialogue between Loic and Paul.
[Loic]: Hello Paul!
[Paul]: Hello Loic!
[Loic]: How are you?
[Paul]: I am fine, thank you!
[Loic]: Goodbye!
[Paul]: Goodbye!
End dialogue between Loic and Paul.
[Paul]: Hello ... Is there anyone?
[Paul]: I'm speaking alone ...
```