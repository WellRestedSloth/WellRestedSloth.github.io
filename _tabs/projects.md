---
# the default layout is 'page'
icon: fas fa-laptop-code
order: 1
---

![sloth_computer_project](/assets/projects/sloth_computer_project.jpg){: width="400" height="400" .shadow }
_Me hard at work_

"Don't ask '***Why?***'.  We should be asking '***Why not?***'!!

When I'm not busy napping high up in a tree, I'm casually working on some of my many hobby projects.  I have some good ideas, and I just need a little bit of time to get them up and running (unlike myself).

I will break down the projects into two groups:
- Building blocks (can be used as part of another larger project)
- Main apps (apps that actually do something useful)

# Building Blocks

These projects can be used as part of a larger application, but they are not usually very useful on their own.

## **Thread Pool (in C)**

(Link to thread pool repository - TBD)

A basic thread pool using Pthreads implemented in the C programming language.  When a caller wants the thread pool to work on a "task", the thread pool queues the "task", waiting for an available worker thread.  Once a worker thread is available the thread pool removes the "task" from the queue and assigns the "task" to one of the available worker threads.  The worker thread works on the "task" until completion.  At this point, the worker thread is now available again to work on other queued "tasks".

Status: Slowly in progress

## **In-Order Callback Data Structure IOCDS (in C)**

(Link to In-Order Callback Data Structure repository - TBD)

This is a data structure (similar to a queue without the caller calling dequeue), where the caller initially registers a callback function.  The callback function gets called when the IOCDS receives or has stored the next expected number.  The caller "pushes" integer numbers to the IOCDS.  The IOCDS stores the numbers internally.  When the next expected number is "pushed", the callback function is called with that number, and the next expected number is incremented by one.  If the IOCDS has stored the next expected number, then the callback function is called with that number, and the next expected number is incremented by one.

The IOCDS can be used to guarantee order if the inputs may not necessarily be in-order.  Similar to how TCP guarantees packet order, the next packet expected would trigger the reception of earlier arriving packets.

Please check the repository description for an example.  The example will explain things better.

Status: Slowly in progress

## **Edsger Dijkstra's Shunting Yard Algorithm**

(Link to Shunting Yard Algorithm repository - TBD)

Ever wondered how a command-line interpreter is implemented?  The shunting yard algorithm is used to convert infix notation to RPN (Reverse Polish Notation), and then executed in order of operator preference.

For example:

Evaluate:
(100 + ( 4 * 3^(10-8)) + max(7*2,10)) / 10

Status: Just a dream for now

## **Lightweight C Logging Header File**

(Link to C Logging Header File - TBD)

This is an implementation of a header-file-only lightweight C logger.  It's designed to be very easy to use.  Just include the logging header file, and use the logging macros in your C source code.

Status: Coming soon!

# Main Apps

These are actual projects that do things!  These projects have a general focus on math, cryptography, or sports-related problems.

## **Factorization and Prime Numbers of Form XX +- YY (in C)**

(Link to XXYYF repository - TBD)

Finding prime numbers and factorizations of the form (X^X + Y+Y) and (X^X - Y^Y).  This is loosely based on the existing XYYXF project (link here).

Status: Slowly in progress

## **Cracking RC5-72 with CUDA (in C)**

(Link to RC5-72-CUDA repository - TBD)

This is an application that attempts to "crack" the RC5-72 RSA Labs contest using CUDA GPU library.

Distributed.net has a CUDA client which is several years old and not as fast as their OpenCL client (in personal testing on my GTX 1060 video card).  This program attempts to find the RC5-72 "key" to decrypt a secret message.  The goal is to make this program faster than the OpenCL version of the Distributed.net client.  You don't know until you try, right?

Status: Just a dream for now

## **NHL Grand Salami Scores Tracker (in Python)**

(Link to Grand Salami Scores Tracker repository - TBD)

In the NHL (National Hockey League), the "Grand Salami" is a wager in which you must correctly guess the "over/under" of the total number of goals scored in every NHL game played that day.  This project uses a Python script to read data from the NHL API to get the current number of goals scored that day.  The script can be used to display today's current NHL scores (like a sports scoreboard with real-time updates), or NHL scores from dates from the past.  The script can also potentially calculate projected number of goals scored, probability of over/under, and other current stats for the day.  This could be expanded to other sports as well (like MLB baseball).

Status: Slowly in progress

## **NHL Grand Salami Odds Tracker (in Python)**

(Link to Grand Salami Odds tracker repository - TBD)

This application reads NHL Grand Salami odds periodically and keeps a history of odds changes.  This data can be used to track scoring trends in the NHL.  In the future, possibly some machine learning can be used to successfully predict the NHL Grand Salami outcome for that day.  This could be expanded to other sports as well (like MLB baseball).

Status: Slowly in progress

## **Grand Salami Tracker Website (in Flask)**

(Link to Grand Salami Tracker Website Project Flask website repositry - TBD)

This website displays live Grand Salami stats (number of goals scored so far that day, odds, predicted outcomes).  This project will bring together the "NHL Grand Salami Scores Tracker" and "NHL Grand Salami Odds Tracker", and display the data in a user-friendly website format.

Status: Just a dream for now

## **Euler-Catalan Conjecture Number Search**

(Link to Euler-Catalan Conjecture repository - TBD)

This project searches for more solutions that satisfy the Euler-Catalan Conjecture.
(More info on Euler-Catalan Conjecture)

Status: Just a dream for now

## **Fake SSH Server (in Python)**

(Link to Fake SSH Server repository - TBD)

This Python project is a "fake SSH" server that listens on port 22.  I noticed that there are a ton of automated bots on the internet that try to guess usernames and passwords on port 22 (the SSH port), constantly bombarding the port with SSH login attempts.  I thought it would be a neat idea to install a "fake SSH" server listening on port 22 and logging the username and password locally.  This data can be displayed real-time on a website.  Of course, the "attacker" would never be able to successfully login, since the SSH server is fake!  An advanced idea would be to "fake" a succesful SSH login, and record the commands the attacker uses, and see what programs the attacker attempts to run.

The "fake SSH" server idea isn't new... other projects on Github call it a "SSH Honeypot".  I want to try to do this myself, and learn about the SSH protocol, and Python socket programming in the process!

Status: Just a dream for now
