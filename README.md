Hello!
Thanks for your application to Zipfian Academy. Please complete the assessment here to accompany your application. Return your answers in email with attachments (1 file per question) to admissions@zipfianacademy.com with the email subject “Technical Assessment: YOUR NAME.”
Please note this assessment is not a pass/fail assignment. We will use your responses to assess your level and if you would be a good fit for our immersive programs. Please submit your responses even if you have not fully completed every part of each question.
We’ll reach out soon with next steps.
Thanks!
Zipfian Academy



Goals
===================================

In this assessment, we will create our own map reduce framework. The overall goal of this assessment will be to ascertain capabilities of multi threading, computer science fundamentals, and understanding of manipulating data at scale (in this case: on multiple cores). 


Resources
===============================

1. Map Reduce: [Data-Intensive Text Processing with MapReduce](http://lintool.github.io/MapReduceAlgorithms/ed1n/MapReduce-algorithms.pdf#page=23)



Setup
==================================================

You will need to install maven. Maven is the standard build system for java.

Under osx, you can do:
           
           brew install maven


Windows, you will need to put mvn in your path. Download a binary release from [here](http://maven.apache.org/download.cgi)

Use the latest release.

After extracting the archive, put the bin folder of maven in your PATH.

If this is unclear, please check:
   
   http://www.computerhope.com/issues/ch000549.htm



Under linux, this will be relative to your distro.

It should be:

     [your-favorite-package-manager] install maven (possibly mvn)
     


Once maven is in your path, please run the following commands:


mvn install:install-file -Dfile=<path-to-file>

where path-to-file is each of the jar files in the test archive.




After installing all the jar files, you are going to want to setup your development environment.


The project should already be setup for you.


Test setup
====================================


Just run the given tests in intellij or use:

       mvn clean test

in the root directory of your project.

The given classes extend the tests that we setup for you. Just run those to verify your output.




Expected Outputs
=======================================

1. You are to implement the given interfaces with the described functionality. 
2. In the word counter implementation, it is required your framework be multi threaded.
3. We are going to run a black box battery of tests, that asserts for correctness as well as speed.
4. You should implement a command line interface with the following parameters:

       -path: the path to the file or directory
      
       -numThreads: the number of threads to use for map reduce
      
       -output: The output file

The output file should look like the following:

      word1    5
      word2    6
 
It should be one word per line with four spaces between the word and the number.


An example of us running the output:

          java -cp "lib/*" -path rootdir -numThreads 8 -output outputfile

We will run our battery of tests against the output file, and implementation tests for correctness and speed.



Testing
=========================================

We will be doing a simple word count over the files.


We will be grading implementation details, efficiency, code quality, and for accurate results.



