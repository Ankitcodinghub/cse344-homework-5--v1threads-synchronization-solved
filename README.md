# cse344-homework-5--v1threads-synchronization-solved
**TO GET THIS SOLUTION VISIT:** [CSE344 Homework #5 –V1Threads synchronization Solved](https://www.ankitcodinghub.com/product/cse344-homework-5-v1threads-synchronization-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93948&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE344 Homework #5 –V1Threads synchronization Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
v1 Threads synchronization

</div>
</div>
<div class="layoutArea">
<div class="column">
This is your final homework for this semester. The idea is to use POSIX threads to parallelize a couple of simple mathematical tasks. Let’s see how much we can accelerate via threads.

<pre>          Example:./hw5 -i filePath1 -j filePath2 -o output -n 4 -m 2
</pre>
Input

The two input files, provided as either relative or absolute paths, will be regular ASCII files of arbitrary content and length.

The process

The process will start by reading the two files into memory. It will read sequentially (2^n)x(2^n) characters (with n provided as a command-line argument, n &gt; 2) from each file. Each character will be converted to its corresponding integer ASCII code equivalent. Every consecutive 2^n characters that it reads will be considered as one matrix row. Therefore, this will lead to reading 2 square matrices A and B of size (2^n)x(2^n) each. If any of the two files has insufficient content, this will be considered a fatal error.

The process will then create m (provided as a command-line argument, m &gt;= 2k, k&gt;=1) POSIX threads. Each thread will have 2 sequential tasks to complete.

a) First, they will calculate C=AxB in a parallel fashion. This means that each thread will be responsible for calculating (2^n)/m columns of C. For example if m=2, then the first thread will calculate the left half of C, and the second thread will calculate the right half of C. This could make the calculation of C twice as fast (with respect to using a single thread)…at least in theory.

b) Once C has been calculated, then the threads will switch to the second task and calculate the 2D Discrete Fourier Transform of C, the same way as before (i.e. (2^n)/m columns calculated by each thread).

Once they have all finished, the process will collect the outputs of each thread and write them to the output file (relative or absolute path), in CSV format (one matrix row per file line). You will report the total time spent, from the moment the files were read into memory, until the calculations were completed. Try your program for various values of n and m, and report your findings in terms of acceleration, if any. Take into account the number of cores on your CPU.

Careful

The threads must wait for each other and not advance to the second part of the calculations before ALL have finished the first part. This is a synchronization ******* (starts with b and ends with arrier). Why? Because in order to calculate each DFT coefficient, you need to access ALL the matrix elements.

Output examples (the numbers are made up – include a timestamp before each output line):

</div>
</div>
<div class="layoutArea">
<div class="column">
Two matrices of size 1024×1024 have been read. The number of Thread 3 has reached the rendezvous point in 0.0123 seconds. Thread 4 has reached the rendezvous point in 0.0121 seconds. Thread 2 has reached the rendezvous point in 0.0119 seconds. Thread 1 has reached the rendezvous point in 0.0124 seconds. Thread 1 is advancing to the second part

</div>
<div class="column">
threads is 4

</div>
</div>
<div class="layoutArea">
<div class="column">
May 11th, 2022

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Thread 4 is advancing to the second part

Thread 3 is advancing to the second part

Thread 2 is advancing to the second part

Thread 1 has has finished the second part in 0.1321 seconds.

Thread 3 has has finished the second part in 0.1212 seconds.

Thread 2 has has finished the second part in 0.1175 seconds.

Thread 4 has has finished the second part in 0.1327 seconds.

The process has written the output file. The total time spent is 0.173 seconds.

Restrictions and requirements

– All threads must run concurrently.

– Solve all synchronization problems only with mutexes and condition variables.

– In case of SIGINT, the process and the threads will terminate gracefully, closing all open files and freeing all allocated resources.

– Calculations will be correct down to 3 decimals.

Evaluation

Your submission will be evaluated with various input files n, m values.

Grading

1) Compilation error: grade set to 1; if the error is resolved during the demo, then evaluation continues.

2) Compilation warning (with respect to the -Wall flag); -1 for every warning until 10. -20 points if there are more than 10 warnings; no chance of correction at demo.

3) No makefile, makefile without -Wall, makefile without “make clean”: -30

4) No pdf report submitted (or submitted but insufficient, e.g. 3 lines of text with no design explanation, etc), file formats other than pdf: -20

5) The program crashes/locks or produces wrong output with valid input: -100

6) Poor synchronization (e.g., sleeps, busy waiting, timed waits, trylocks, etc): -100

7) The program doesn’t satisfy a requirement or violates a restriction: -100

8) Presence of memory leak (regardless of amount – checked with valgrind) -30

9) No late submissions.

10) In case of an arbitrary and fatal error, exit by printing to STDERR a nicely formatted informative message. Otherwise: -10

11) If you don’t cleanup after children processes and/or leave zombies: -50

</div>
</div>
</div>
