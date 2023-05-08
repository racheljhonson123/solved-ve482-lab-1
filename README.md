Download Link: https://assignmentchef.com/product/solved-ve482-lab-1
<br>
<h1>1         Hardware overview</h1>

<strong>Some components might be missing, in such a case figure out their expected location.</strong>

In the computer locate:

<table width="585">

 <tbody>

  <tr>

   <td width="389">•     The motherboard•     A Hard Disk Drive•     An Optical disk driveOn the motherboard locate:</td>

   <td width="197">•     The PC power supply•     A PCI card</td>

  </tr>

  <tr>

   <td width="389">•     The RAM•     A SATA socket•     A PCI/PCI-e slot•     The CPU</td>

   <td width="197">•     The North and South bridges•     The battery•     The BIOS</td>

  </tr>

 </tbody>

</table>

Answer the following questions:

<ul>

 <li>Where is the CPU hidden, and why?</li>

 <li>What are the North and South bridges?</li>

 <li>How are the North and South bridges connected together?</li>

 <li>What is the BIOS?</li>

 <li>Take out the CPU, rotate it and try to plug it back in a different position, is that working?</li>

 <li>Explain what overclocking is?</li>

 <li>What are pins on a PCI/PCI-e card and what are they used for?</li>

 <li>Before PCI-e became a common standard many graphics cards were using Accelerated Graphics Port (AGP), explain why.</li>

</ul>

<h1>2         Git</h1>

Register on our git server at <a href="http://focs.ji.sjtu.edu.cn/git">http://focs.ji.sjtu.edu.cn/git</a>. We will use this git server all along the semester. For the various group projects student <strong>must use git</strong>: part of their grade will be based on their commits. Please closely follow the TAs’ instructions and ensure your are fully setup for the rest of the semester. In particular by the end of the lab <strong>you should have uploaded your ssh public key </strong>on Gitea.

Basic git usage will be studied in a future lab. In the meantime get familiar with:

<ul>

 <li>Opening and using issues;</li>

 <li>Simple commands such as clone, commit, push, and pull;</li>

 <li>Using the Wiki and markdown, they will be used for the projects documentation;</li>

</ul>

<h1>3         Command line interface</h1>

The goal of this part of the lab is to get use of the terminal and command line interface. The command line interface is often faster that graphical user interfaces as there is no need to move the mouse around to click in many “random places” on the desktop; commands are usually simple and well documented.

We start by briefly explaining how to perform basic tasks and then move on to writing simple <em>shell scripts</em>. A shell script is a program meant to be run by the command line <em>interpreter</em>; it often consists in a list of command lines together with some loops and conditional statements, everything being stored in a file with a .sh suffix.

Scripts have many usages and can really simply life when facing repetitive tedious tasks. Common example of such tasks are automatically updating and generating slides every semester, automatically uploading documents and setting up assignments on Canvas, or even filling in the Honour Council form in case of cheating suspicions.

Knowing the basics on how to use the command line interface to write simple scripts can highly simplify your life all along your studies and even in your future career.

<h2>3.1        Basic Unix commands</h2>

Simple commands to run basic tasks:

<ul>

 <li>Directory tree navigation: ls, cd Text manipulation: echo, cut</li>

 <li>File and directory manipulation: mv, rm, cp, Search: find, grep</li>

</ul>

<sup>mkdir, rmdir </sup>• Navigate through the command history: up • File reading: cat, head, tail and down keys, ctrl-r

To access the manual on each of the above command use man, e.g. man ls. To navigate in the documentation use the direction keys or search for some keyword, e.g. once in the ls manual, type /author. You will then jump to the first occurrence of the word “author”. Press n to jump to the next one and N for the previous one.

Some manual pages can be very very long (several thousands of lines), so do not waste time reading from the beginning to the end. Instead use keywords to search or scan through it. An online search can also help pinning down the correct parameters.

Various shells exist with more of less features and slightly different syntax. Being familiar with one should allow you to be comfortable with others. The most common ones are dash (basic shell), bash and zsh which both have many features. Most Linux distributions use bash as default and macOS recently moved from bash to zsh.

For the sake of simplicity in the following guidelines we focus on bash, but all the tasks can be completed using zsh or dash if you prefer.

<h2>3.2        Shell scripting</h2>

Some basic shells such as mumsh, the shell developed in VE482, are simple command line interfaces without any real programming features. All the previously mentioned, dash, bash, and zsh, in fact implement a fully features programming language best used for writing scripts. The following information remain very basic and minimalistic, numerous other powerful features being available. Feel free to poke around the man page to learn more or direct your attention to other important topics such as <em>regular expressions</em>, or sed and awk.

To run a shell script open a terminal and simply type interpreter scriptname, where interpreter is the name of your shell, e.g. bash or zsh, and scriptname is the name of your script (often ending with .sh).

<h3>3.2.1        Basics</h3>

<h3>3.2.2        Conditional statements</h3>

<h3>3.2.3        Loops</h3>

<h3>3.2.4        Arrays</h3>

<h3>3.2.5        Functions</h3>

<h2>3.3        Tasks</h2>

<em>After this brief introduction lets play with the shell!</em>

Answer the following questions, only refering to man pages:

<ul>

 <li>Use the mkdir, touch, mv, cp, and ls commands to:

  <ul>

   <li>Create a file named test.</li>

   <li>Move test to dir/test.txt, where dir is a new directory.</li>

   <li>Copy dir/test.txt to dir/test_copy.txt.</li>

   <li>List all the files contained in dir.</li>

  </ul></li>

 <li>Use the grep command to:

  <ul>

   <li>List all the files form /etc containing the pattern 127.0.0.1.</li>

   <li>Only print the lines containing your username and root in the file /etc/passwd (only one grep should be used)</li>

  </ul></li>

 <li>Use the find command to:

  <ul>

   <li>List all the files from /etc that have been accessed less than 24 hours ago.</li>

   <li>List all the files from /etc whose name contains the pattern “netw”.</li>

  </ul></li>

 <li>In the bash man-page read the part related to redirections. Explain the following operators &gt;, &gt;&gt;, &lt;&lt;&lt;, &gt;&amp;1, and 2&gt;&amp;1 &gt;. What is the use of the tee</li>

 <li>Explain the behaviour of the xargs command and of the | operator.</li>

 <li>What are the head and tail commands? How to “live display” a file as new lines are appended?</li>

 <li>How to monitor the system using ps, top, free, vmstat?</li>

 <li>What are the main differences between sh, bash, csh, and zsh?</li>

 <li>What is the meaning of $0, $1,…, $?, $!?</li>

 <li>What is the use of the PS3 variable? Provide a short code example.</li>

 <li>What is the purpose of the iconv command, and why is it useful?</li>

 <li>Given a variable $temp what is the effect of ${#temp}, ${temp%%word}, ${temp/pattern/string}.</li>

 <li>Search online (not on the man pages), how files are organised on a Unix like system. In particular explain what are the following directories used for:</li>

</ul>

<table width="586">

 <tbody>

  <tr>

   <td width="496">–    /   <strong>– </strong>/lib <strong>– </strong>/usr/lib   <strong>– </strong>/srv–    /bin <strong>– </strong>/mnt <strong>– </strong>/usr/src   <strong>– </strong>/media–    /boot     <strong>– </strong>/usr/bin   <strong>– </strong>/proc      <strong>– </strong>/opt–    /etc <strong>– </strong>/usr/share <strong>– </strong>/sys <strong>– </strong>/var<em>Now lets write some real scripts!</em></td>

   <td width="91">–    /sbin–    /dev–    /vmlinuz–    /initrd.img</td>

  </tr>

 </tbody>

</table>

Write a game where the computer selects a random number, prompts the user for a number, compares it to its number and displays “Larger” or “Smaller” to the user, until the player discovers the random number initially chosen by the computer.

<em>Hints: </em>the following commands might be helpful.

<ul>

 <li>echo $RANDOM $((10%3))</li>

 <li>man read</li>

 <li>To search in a man page some characters need to be <em>escaped</em>, e.g. to search for $((, do /$((</li>

 <li>Above commands might have to be adjusted to meet the requirements and avoid bugs</li>

</ul>