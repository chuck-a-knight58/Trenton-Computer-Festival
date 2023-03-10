[Trenton Computer Festival 2022](https://tcf-nj.org/)

#### Introduction to Python

Python is a very powerful programming language used in a variety of engineering and scientific settings.
Its popularity has spread in recent years mainly due to its ease of use and large collection of support libraries.

In this talk I'll provide a gentle introduction to the language using a hands on, demonstrative approach.
By the end of this talk, attendees should know how to get started with writing simple scripts in Python, and
have a general understanding of the Python ecosystem.

Jupyter notebook is here 
https://github.com/chuck-a-knight58/Trenton-Computer-Festival 

Notebooks published to and hosted on Binder are available for in browser use 
https://mybinder.org/v2/gh/chuck-a-knight58/Trenton-Computer-Festival/master

Double click the file "Introduction to Python.ipynb" once Jupyter starts.


#### Pythonic Object Oriented Development

Object-Oriented Programming is a widely used concept to write powerful applications in many languages.

In this talk tackle the basics of Object-Oriented Programming in Python: exploring classes, objects, instance 
methods, attributes and much more!

Jupyter notebook is here 
https://github.com/chuck-a-knight58/Trenton-Computer-Festival 

Notebooks published to and hosted on Binder are available for in browser use 
https://mybinder.org/v2/gh/chuck-a-knight58/Trenton-Computer-Festival/master

Double click the file "Pythonic Object Oriented Development.ipynb" once Jupyter starts.

A more comprehensive list of special methods can be found in special-method-names.htm

#### Program your EV using Python and ODB-II

With Python and a simple $20 bluetooth device you can gain access to your electric vehicles real-time sensor data using its OBD-II vehicle ports. During this seminar we'll show you how to:

* Setup and configure your python environment
* Access your vehicles trouble codes
* Access realtime data about your vehicle
* Perform simple hacks to the operation of your vehicle

Jupyter Notebook is here
TBD

Notebooks published to and hosted on Binder
TBD

Double click the file "Program your EV using Python and ODB.ipynb" once Jupyter starts.

Required packages:

    pip install obd
    pip install ELM327-emulator

##### What is OBD

On-board diagnostics (OBD) is a term referring to a vehicle's self-diagnostic and reporting capability. OBD systems give the vehicle owner or repair technician access to the status of the various vehicle sub-systems. The amount of diagnostic information available via OBD has varied widely since its introduction in the early 1980s versions of on-board vehicle computers. Early versions of OBD would simply illuminate a malfunction indicator light (MIL) or "idiot light" if a problem was detected, but would not provide any information as to the nature of the problem. Modern OBD implementations use a standardized digital communications port to provide real-time data in addition to a standardized series of diagnostic trouble codes, or DTCs, which allow a person to rapidly identify and remedy malfunctions within the vehicle.

OBD-II provides access to data from the engine control unit (ECU) and offers a valuable source of information when troubleshooting problems inside a vehicle. The SAE J1979 standard defines a method for requesting various diagnostic data and a list of standard parameters that might be available from the ECU. The various parameters that are available are addressed by "parameter identification numbers" or PIDs which are defined in J1979. For a list of basic PIDs, their definitions, and the formula to convert raw OBD-II output to meaningful diagnostic units, see OBD-II PIDs. Manufacturers are not required to implement all PIDs listed in J1979 and they are allowed to include proprietary PIDs that are not listed. The PID request and data retrieval system gives access to real time performance data as well as flagged DTCs. For a list of generic OBD-II DTCs suggested by the SAE, see Table of OBD-II Codes. Individual manufacturers often enhance the OBD-II code set with additional proprietary DTCs.

https://en.wikipedia.org/wiki/OBD-II_PIDs

##### Setup and Initial Connection

    To enable the preconfigured set of OBD service requests of a Toyota Auris Hybrid car, run the emulator with the -s car option:
    
        python -m elm -s car

    Verify the port the emulator is using to communicate on. This port should be used
    when creating a OBD communications object for querying the car's OBD system. Normally, this package would scan for any active bluetooth or serial connections and automatically use them:

        CMD> port
        Using pseudo-tty port "/dev/pts/2".

    Test your connection:

        import obd
        connection = obd.OBD("/dev/pts/2")
        cmd = obd.commands.SPEED
        response = connection.query(cmd)
        print(response.value)

##### Data Organization


Resources
https://en.wikipedia.org/wiki/On-board_diagnostics#OBD-II
https://forscan.org/forum/viewtopic.php?f=5&t=836 (software for Ford vehicles)

https://github.com/Ircama/ELM327-emulator (an ELM327 emulator)

    python3 -m pip install ELM327-emulator


https://icculus.org/obdgpslogger/obdsim.html
https://github.com/brendan-w/python-OBD

#### Recommended Reading

[Practical Python Design Patterns: Pythonic Solutions to Common Problems 1st ed. Edition](https://www.amazon.com/Practical-Python-Design-Patterns-Solutions/dp/1484226798)

[PEP8 Python Style Guide](https://www.python.org/dev/peps/pep-0008/)


#### A Python Easter Egg

```
[GCC 4.2.1 Compatible Clang 4.0.1 (tags/RELEASE_401/final)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import this
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
>>>
```

chuck.a.knight@gmail.com
