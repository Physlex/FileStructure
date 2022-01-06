#This is supposedly the proper way to use modern cmake, with the focus
#being on subdirectories and section - per - section code as well as
#cmake - specific functions

cmake_minimum_required(VERSION 3.7...3.22) #Allows for cmake to be worked within a range

if(${CMAKE_VERSION} VERSION_LESS 3.12) #If the current version of cmake is less than the VESION_LESS keyword defined value of cmake then;
  cmake_policy(VERSION ${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION}) #The policy is set to the current cmake version
endif() #The only language I have ever used that needs to define the end of an if statement as a function / macro. Interesting.

#Basically sets up the project to be properly defined in software engineering terminology like version control and early documentation
project(CmakePropah VERSION 0.8 DESCRIPTION "A project to properly understand the basics of modern cMake" LANGUAGES CXX)
