# GraphTheory-2017-Project
3rd Year Under-graduate graph theory project using Neo4J

## Introduction

The structure in which this graph db is broken up into are as follows:
| Name | Type | Relationship | Receiver |
| ------ | ------ | ------ | ------ |
| Day | Node | Null | null |
| Room | Node | Time | Day |
| Module | Node | Lab / Lecture | Room |
| Module | Node | Is in | Years |
| Year | Node | null | null |
| Course | Node | Has | Years |
| Lecturer | Node | Teaches | Module |

In this project we we're tasked wih taking our timetable and putting it into a graph database.
I decided to take the course as a whole and display the time table for all with clear segementation of years and what is in each year.
Before building the graph I decided that it would be best to record all data that would be required in a text file. 
From data mining I extracted modules, rooms, lecturers. I then filtered this data down to the relevant data required for the task, removing rooms, & lecturers and began to build my queries from this.

## Structure

When approaching the problem I took some time to draw out and plan how the data should be represented.
I had come to 4 different con clusions on how I might approach the problem seen below.

![123](http://imgur.com/5YqFuIo.png)
![4](http://imgur.com/FkuX635.png)

I ended up opting for the 4th option as this seemed to be the most logical, although there are many other viable routes I could have taken
when building this database. 

The structure in english is as follows: The course has multiple years which each have their modules that are taught by lecturers, the modules have labs & lectures in rooms at times of the day. 
###### (Course)-[Has]->(Year)<-[In]-(Module)-[Lab / Lecture]->(Room)-[Time]->(Day).

With that structure in mind I began to datamine extracing only the most relevant information which I required to build the graph.
Once the dataminig was done I then began to research how to make nodes, relationships, labels, properties, etc.
After some experimentation I was ready to begin building the graph. 

Rather than jumping straight into the console I decided to build up all the queries into a text file which I could simply copy and paste into the console...

This also gave me the idea that with a simple script could be written to automate the process, while I did follow through on writing the script due to time constraints, I do think this would be a simple enough task essentially the script would read from a file and write to the console.

The text file which I spoke of is attached to this git repository named GraphTheoryProj.txt for your interest.
Half the point of writing this was that if there were any issues during the build of the database all queries were easily available for future use. 

See the graph in it's final form here:
(graph)[http://imgur.com/a/trOJH.png]



## Conclusion

While I do feel that I've only scraped the surface of what Neo4J can offer, I feel like I have learned quite a bit, & would reconsider 
the structure in which I have used in this prototype. I also believe there could be far more effecient ways of querying the console to make the process a little less repetitive.

 
