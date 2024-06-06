# Tasks 102: Testing for Mahfil App
# Mahfil Mobile App Manual Testing
# Table of Contents:
Introduction
Test Plan
Test Schedule
Test Mindmaps
Test Cases
Bug Report 
# Introduction:
This manual testing project for the Mahfil mobile app covers essential topics such as test plans, test schedules, mind maps, test cases, reports, and bug tracking using JIRA. The aim is to provide a comprehensive and organized approach to ensure the app's quality and reliability.

# Test Plan:
The test plan acts as a rule book for testing the Mahfil app. It outlines the scope and approach, identifies risks, and helps mitigate them. The test plan includes:
![image](https://github.com/aopi74/Assignment_Steadfast_IT/assets/85184571/fbc719f7-0263-4fa2-b838-7d6f4c6b1e66)



# Product analysis
Test strategy development
Defining test objectives
Establishing test criteria
Resource planning
Setting up the test environment
Estimation
Release and test deliverables
# Test_Scenarios:
The test Test scenarios list all activities, tasks, and events in the test process, along with their intended start and finish dates/times and dependencies.

![image](https://github.com/aopi74/Assignment_Steadfast_IT/assets/85184571/87beb798-26cc-453e-a455-7a7ad542ef51)

# Test Mindmaps:
Mindmaps visually represent test coverage, dependencies between features and modules, and areas to focus on during testing.
![image](https://github.com/aopi74/Assignment_Steadfast_IT/assets/85184571/dc9574b2-17e3-4be2-b67c-50190d720de9)

# Test Cases:
Test cases verify that the application operates as expected. Each test case includes:

Test case ID
Test case description
Expected result
Actual result
Test data
Reproducing steps
Bug screenshots
Status
![image](https://github.com/aopi74/Assignment_Steadfast_IT/assets/85184571/bfbf5217-8138-42c1-b411-79ae6c0d9481)

# Test Report:
Test reports may include defect reports, test execution reports, test summary reports, and other relevant documentation.
![image](https://github.com/aopi74/Assignment_Steadfast_IT/assets/85184571/5257ed95-bd23-4ea1-8c89-2333774fa6da)

# Bug Report 
JIRA is used for tracking and reporting bugs. It helps report bugs to developers and track their resolution.
![image](https://github.com/aopi74/Assignment_Steadfast_IT/assets/85184571/0f06a787-3c16-4174-8f61-810118a46adc)

# Tasks 102: Java Program for Word Count

# Detailed Explanation
Class Declaration

public class SteadfastIT {
The SteadfastIT class is declared as public, meaning it can be accessed from other classes.
# Main Method


public static void main(String[] args) {
The main method is the entry point of the program. It is public, static, and void with String[] args as its parameter to accept command-line arguments.
# File Path

String filePath = "input.txt";
The path to the input text file (input.txt) is stored in the filePath variable.
# TreeMap Declaration


Map<String, Integer> wordCountMap = new TreeMap<>();
A TreeMap named wordCountMap is created to store word counts. A TreeMap maintains the order of its keys, ensuring the words are stored in alphabetical order.
# Reading the File

try (BufferedReader reader = new BufferedReader(new FileReader(filePath))) {
    String line;
    while ((line = reader.readLine()) != null) {
A BufferedReader wrapped around a FileReader is used to read the file line by line.
The try-with-resources statement ensures the reader is closed automatically after use.
# Processing Each Line


String[] words = line.split("\\s+");
Each line is split into words using whitespace (\\s+) as the delimiter.
# Processing Each Word

for (String word : words) {
    
    word = word.replaceAll("[^a-zA-Z]", "").toLowerCase();
Each word is processed to remove any non-alphabetic characters using replaceAll("[^a-zA-Z]", "").
The word is then converted to lowercase using toLowerCase().
# Updating the Word Count

if (!word.isEmpty()) {
    wordCountMap.put(word, wordCountMap.getOrDefault(word, 0) + 1);
}
If the word is not empty, its count is updated in the wordCountMap.
wordCountMap.getOrDefault(word, 0) retrieves the current count of the word (or 0 if the word is not yet in the map) and increments it by 1.
# Error Handling


} catch (IOException e) {
    System.err.println("Error reading the file: " + e.getMessage());
}
If an IOException occurs (e.g., if the file cannot be read), an error message is printed to the standard error stream.
# Displaying Word Counts


for (Map.Entry<String, Integer> entry : wordCountMap.entrySet()) {
    System.out.println(entry.getKey() + ": " + entry.getValue());
}
The word counts are displayed in alphabetical order.
wordCountMap.entrySet() returns a set of key-value pairs, and each pair is printed in the format word: count.

#  flowchart
![Uploading image.png…]()


