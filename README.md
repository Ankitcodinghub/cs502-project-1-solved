# cs502-project-1-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/cs502-introduction-solved/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;128528&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS502 Project 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
<div class="kksr-stars">
    
<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
    
<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>
                

<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
This assignment is intended to introduce you to the process manipulation facilities in the Linux Operating System, which originate from the Unix Operating System from which Linux is a dialect. You are to implement the program described below on a Linux machine. The program needs to be implemented in C or C++ and compiled with gcc or g++.

Command Execution

You are to write a program doit that takes another command as an argument and executes that command. For instance, executing:

% ./doit wc foo.txt

would invoke the wc “word count” command with an argument of foo.txt, which will output the number of lines, words and bytes in the file “foo.txt” (which is assumed to exist in the current directory). Note the wc command will work on any file containing text. After execution of the specified command has completed, doit should display statistics that show system resources the command used. In particular, doit should print:

1. the amount of CPU time used (both user and system time) (in milliseconds),

2. the elapsed “wall-clock” time for the command to execute (in milliseconds),

3. the number of times the process was preempted involuntarily (e.g. time slice expired,preemption by higher priority process),

4. the number of times the process gave up the CPU voluntarily (e.g. waiting for a resource),

5. the number of major page faults, which require disk I/O, and

6. the number of minor page faults, which could be satisfied without disk I/O.

7. the maximum resident set size used, which is given in kilobytes.

Basic Command Shell

exit—causes your shell to terminate. cd dir—causes your shell to change the directory to dir.

set prompt = newprompt—causes your shell to change the prompt to newprompt. The prompt is one of many shell variables that an actual shell will maintain, but this is the only one you need to handle in your shell.

&lt; current directory is changed to dir (if successful) &gt; ==&gt;ls

&lt; listing of files in the current directory &gt;

&lt; statistics about this ls command &gt; ==&gt;set prompt = myprompt:

&lt; change string used for your shell prompt &gt;

myprompt:exit

% &lt; back to the shell prompt &gt;

Background Tasks

For the final two points of the project, you need to extend your basic command shell to handle background tasks—you should not create a new executable for this portion of the project. A background task is indicated by putting an ampersand (‘&amp;’) character at the end of an input line. When a task is run in background, your shell should not wait for the task to complete, but immediately prompt the user for another command. Note that any output from the background command will be directed to the terminal display and will intermingle with output from your shell and other commands.

With background tasks, you will need to modify your use of the wait() system call so that you check the process id that it returns. The returned process id might correspond to a background task rather than the currently invoked foreground task. In this case, your shell should print out the process id of the completed background task along with the command name. You also need to add an additional built-in command to your shell:

jobs—lists all background tasks

A sample session with background tasks is given below with comments given in &lt;&gt;.

% ./doit

==&gt;sleep 5 &amp;

[1] 12345 &lt; indicate background task and its process id &gt;

==&gt;jobs

[1] 12345 sleep &lt; print process id and command name for tasks &gt;

==&gt;ls

&lt; listing of files in the current directory &gt;

&lt; statistics about this ls command &gt;

==&gt;cat foo.txt

[1] 12345 Completed &lt; indicate that the background jobs is complete &gt;

&lt; statistics about this sleep command &gt;

&lt; print the file foo.txt &gt;

&lt; statistics about this cat command &gt;

==&gt;exit

% &lt; back to the shell prompt &gt;

If the user tries to exit the shell before all background tasks have completed then your shell should refuse to exit and wait() until these tasks have completed.

You should also observe how your mini-shell works in comparison to a regular Linux shell. Does it have all the same features? What limitations does it have? You should include your observations as a comment in your code that is turned in.

Helpful Hints

The following system calls might be useful:

fork() — create a new process.

To get help information about these routines, use the Linux “man” command. For instance, entering “man fork” will display the manual page entry for fork on the terminal. The manual pages are organized into sections. Section 1 is for Linux commands, Section 2 is for system calls and Section 3 is for library routines. Some entries are contained in more than one section. For example to obtain information about the system call wait() (rather than the command wait) use “man 2 wait” where the section is explicitly given.

Submission of Assignment

Submit your project as directed in class using the assignment name “proj1”. At a minimum you should submit your program code and a file showing execution of your program on test cases for your program. The script command is useful for doing so.
