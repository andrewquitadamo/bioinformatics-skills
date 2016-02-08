#Make and Makefiles
This lesson is to introduce you to Make, and how you can use it for reproducible research.

#Make

Make was originally used to build and install packages from source code

However we can use it to document our analyses, and create reproducible workflows

Make allows you to specify dependancies, and the exact steps required to create the files you need.

Make comes intalled on most *nix systems

#Makefiles

The instructions that Make runs are placed into a Makefile

It is a plain text file named "Makefile" or "makefile"

It specifies the targets, dependancies and steps to run

#Makefile Structure

A simple rule has this structure:
```
target: dependancy
	instructions
```

The instructions line is indented with a hard tab ("\t") and not spaces.

#Your first Makefile

We will start by downloading a file using the command line

The target will be the file name, in this case `SV_gene_sample`

Since we are downloading the file, there are no dependancies

The instructions will be what we would normally run on the command line
`curl https://raw.githubusercontent.com/andrewquitadamo/bioinformatics-skills/master/data/01-command-line/SV_gene_sample -O`

**Instructions**  
Create a new Makefile with a rule to download `SV_gene_sample`

#Running Make

To execute the rules in a makefile, use the `make` command in the command line

Make will only execute a rule when necessary. If a target already exists, and none of its dependancies have been updated make won't do anything

**Instructions**
Run `make`. Check to see if the file was created.
Try to run `make` again. It should tell you that everything is up to date

#Adding multiple rules

If you could only specify one rule in a Makefile, that would be pretty useless

Thankfully you can add as many rules as you want

**Instructions**
Add a new rule to create a file called `SV_list`
Use `cut -f 1 SV_gene_sample | sort | uniq > SV_file` as the command
Run `make`. Make will tell you everything is up to date, but no new file has been created.

#What happened?

By default Make only executes the first rule, so we have to modify our Makefile to get both rules to run.

The easiest way to do this is to add a new rule at the top of the file.

Traditionally this rule is called `all`.

**Instructions**
Add an `all` rule to the top of your Makefile.
Makesure to specify `SV_list` as a dependancy

#Even More Rules

Lets add a new rule to create a file called `gene_list`.
The command should be `cut -f 2 SV_gene_sample | sort | uniq > gene_list`

**Instructions**
Add the new rule.
Run `make`. Make should say everything is up to date.
Add `gene_list` as a dependancy to `all`
Run `make`

