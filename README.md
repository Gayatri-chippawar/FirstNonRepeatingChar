# 🔡 First Non-Repeating Character in a Stream (Queue-Based Approach)
## 📌 Overview

This project implements a Queue-based algorithm in Java to find the first non-repeating character in a stream of characters.

As each character is processed from the string, the program prints the first character that has appeared only once so far. If no such character exists at that moment, it prints -1.

This is a classic Data Structures & Algorithms (DSA) problem combining:

Queue (FIFO)

Frequency Array

Character Stream Processing

## 🚀 Problem Statement

Given a string representing a stream of lowercase characters, print the first non-repeating character at each step of the stream.

If no non-repeating character exists, print -1.

Example

Input:

aabccxb

Output:

a -1 b b b b x
## 🧠 Approach

The solution uses:

1️⃣ Frequency Array
int[] freq = new int[26];

Tracks occurrences of each lowercase character (a-z).

Index mapping: ch - 'a'

2️⃣ Queue
Queue<Character> q = new LinkedList<>();

Stores characters in order of arrival.

Helps track the first non-repeating candidate.

## ⚙️ Algorithm Steps

For each character in the string:

Add character to queue.

Increment its frequency.

While:

Queue is not empty AND

Front character frequency > 1
→ Remove it from queue.

If queue becomes empty → print -1

Else → print q.peek() (first non-repeating character)

## ⏱ Time Complexity

O(n)
Each character is:

Added to queue once

Removed at most once

## 💾 Space Complexity

O(1)
Frequency array size = 26 (constant)

O(n) worst case for queue

## 📚 Concepts Used

Queue (FIFO principle)

Frequency counting

Character indexing

Stream processing

Greedy elimination logic

## 🎯 Key Learning

This problem demonstrates how combining:

A frequency counter

With a queue for order tracking

can efficiently solve real-time stream-based problems in linear time.

## 🛠 Requirements

Java 8+

Basic understanding of:

Arrays

Queue (LinkedList)

Character arithmetic
