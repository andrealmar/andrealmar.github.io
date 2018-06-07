---
title: "How to setup ATOM as your Python development environment"
description: How to setup ATOM as your Python development environment
header: How to setup ATOM as your Python development environment
---

PyCharm is an awesome IDE for Python Development and I use it a lot. But sometimes it gets soooo heavier that I want to kill myself. Then I’ve found ATOM. ATOM is a coding editor created by the GitHub team with the goal to be simple, powerful and highly customizable.

There are some features that I really like in ATOM like:

- Built-in package manager
- Multiple panes
- File system browser

If you want to give it a try and use ATOM as your Python development environment, keep reading and I’ll show you how I configure my ATOM settings to make easier for us Python developers to have a very simple and powerful development environment.

I’m using a Macbook so I’m assuming you are using one too. Hit `Command + ,` and this will bring the Settings tab. If you use another OS change the `Command` key to `Ctrl` key.

In Editor Settings, check the `Back Up Before Saving` box. This will avoid corrupt files in case of failure during file save process.

Go below and check the `Show Indent Guide` and `Show Invisibles` boxes. This options will help you navigate through your code showing the indentation. This is very helpful specially when you are working with Web Development and HTML files.

On the left Menu, click on Install option. We are going to install the following packages:

- linter-flake8
- linter-pep8
- autocomplete-python
- django-templates

The installation is pretty straightforward, you search for the package and after you’ve found it you click on Install. It’s simple as that.

After that, your ATOM will be ready to rock some Python code. But we are not finished yet. If you try to open a Python project using ATOM you will notice that things are not working well.

![](/img/atom-python.png "Atom")

This happens because ATOM uses `pep8`, `flake8` and `jedi` packages in its plugins. That’s why we need to install those Python packages.

You already created your Python Virtual Environment following the best practices right? If so we are going to install the following Python packages:

{% highlight python  %}
source venv/bin/activate
{% endhighlight %}

In my case venv is the name of my Virtualenv environment.

More on Virtualenv’s here: http://docs.python-guide.org/en/latest/dev/virtualenvs/

Now proceed with the installation of the Python packages:

{% highlight python  %}
pip install pep8 flake8 jedi
{% endhighlight %}

And we’re done. Very simple and you will have your ATOM editor ready to use as your Python Development environment

See ya !!!
