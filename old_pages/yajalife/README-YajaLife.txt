YajaLife, v1.0

WHAT IS IT?

YajaLife ("Yet another Java A-Life") is a cross-platform artificial
life / cellular automaton simulator / game written in Java. It is
inspired by several principles and ideas used in the well-known a-life
programs Tierra and Avida.

YajaLife is a world of resources and "bugs" that utilize the
resources. The more capable a bug is at utilizing the resources in the
world, the more fit it is and the longer it has to pass on its genes
to the next generation.

The bugs are small agents that can move about in the world of
resources and interact with it and with each other. Each bug is in
essence a small "virtual CPU" that contains a small number of memory
registers, one or more stacks, and an I/O buffer. The genome in each
bug is a small program loop with instructions that tell the bug how to
process sensory input, act in response to its inputs and registers
(e.g. by moving around in the world), manipulate values in its
registers, stacks and buffers, step around in its program, and
allocate memory and duplicate its instructions in order to
reproduce. The population of bugs is seeded with a basic genome
(program) that is capable only of duplicating itself (and thus
creating another similar genome). The execution of any program is not
perfect, and therefore errors may be introduced in the child's
program/genome during copying that may make it more or less capable of
utilizing resource(s) in the environment. If it is more capable, the
population quickly grows and starts using all of the resources in the
environment very quickly. 

A bug is "born" with a fixed number of CPU cycles; in other words it
is capable of executing a fixed number of instructions in its
genome/program. In order for it to survive (and reproduce) longer than
its competitors, it must take advantage of the resources in the
environment.

The resources themselves are also small programs (subroutines, really)
that take input values and return output values, for example, "a + b /
2". For a bug to "use" this example resource, it must first write any
two values into its I/O buffer and then write a 3rd value, which is
the first plus one-half of the second. If it is capable of "executing"
this "resource", it obtains that resource's "reward", which are
additional "CPU cycles" that add to its life span. The use of
resources like this allow for a continually changing environment for
the bugs that may increase in complexity with no limit. The more
complex a resource's program is to execute, the greater its reward.

As the simulation progresses, more and more complex bugs evolve that
move around in the environment and are capable of executing more and
more complex resources.

The bugs' genomes and the resource programs instructions are
translated through a flexible dictionary class that translates the
values in the programs into actual instructions. This allows for a
quick modification and/or addition of the instruction set for
different simulations (or even allowing the dictionary to change with
time during a single simulation!). All parameters and instructions
(including the seed program) are configured via text files that are
read in at the beginning of the run. Finally, the program allows for
regular checkpointing and taking of screenshots, as well as selecting
individual agents in the grid to print out or save its program at any
time.

The application's screenshot capability requires the Gif encoder from
Acme Labs' Java library (http://www.acme.com/java/software/
Acme.JPM.Encoders.GifEncoder.html).  To run or compile this package,
fetch the Acme Labs' jar file "acme.jar" from http://koala.ilog.fr/
ftp/pub/acme.jar (read the BSD-style license at http://www.acme.com/
license.html), and add it to your Java classpath.

_______________________________________________________________________

TO COMPILE:

See the note above about the Acme Java library.

Install a Java DK (anything older than Java 1.1 will work).

Edit the Makefile if necessary.

Type "make" to create "yajalife.jar".

_______________________________________________________________________

TO RUN:

See the note above about the acme.jar library.

Type "appletviewer yajalife.html"... OR ...

Open yajalife.html in a Java-enabled web browser... OR ...

Type "java -jar yajalife.jar 1"... OR ...

Type "yajalife.sh" (if running Linux) or double click "yajalife.bat"
(if running Windows).

_______________________________________________________________________

Additional information:

I believe that others may learn from and use the simulation. There are
many more features and additions that could be added to the program to
make it more complex and enable more interesting resulting
evolution. I would be happy to work with anyone who would be
interested in pursuing this. Some ideas I have are listed in the TODO
program, and in various comments throughout the programs source code.

The source code is distributed under the GPL (see COPYING).

------------------------------------------------------------

