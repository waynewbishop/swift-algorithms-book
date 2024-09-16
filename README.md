# Swift Algorithms & Data Structures, 5th Edition

Swift, first introduced by Apple in 2014, has quickly become a cornerstone of iOS, macOS, watchOS, and tvOS development. With over a decade of evolution and refinement, Swift is now the primary language for building apps across Apple's ecosystem. It's used daily by developers worldwide to create everything from simple utility apps to complex, data-driven applications. This project provides a framework for commonly used data structures and algorithms written in Swift, offering practical implementations that go beyond the pseudocode or C/C++ examples often found on Wikipedia.

## Audience

As a developer, you should already be familiar with the basics of programming. Beyond algorithms, this project also aims to provide an alternative for learning the basics of Swift. This includes implementations of many Swift-specific features such as optionals, extensions, protocols and generics. Beyond Swift, audiences should be familiar with **Singleton** and **Factory** design patterns along with sets, arrays and dictionaries.

## Table of Contents

1. [Introduction](book/chapters/01_introduction.md)
2. [Big O Notation](book/chapters/02_big_o_notation.md)
3. [Basic Sorting](book/chapters/03_basic_sorting.md)
4. Advanced Sorting
5. Generics
6. Linked Lists
7. Tries
8. Stacks & Queues
9. Binary Search Trees
10. Tree Balancing
11. Graphs
12. Shortest Paths
13. Heaps
14. Traversals
15. Blockchain Design
16. Hash Tables
17. Machine Learning
18. Closures
19. Control Structures
20. Recursion
21. Dynamic Programming
22. Unit Testing
23. Objective-C Primer
24. [Exercise Solutions](book/chapters/24_exercise_solutions.md)

## The Book

Now in its **5th edition** and supporting the latest version of Swift, the Swift Algorithms Book features code and color illustrations that benefits students and professionals. As a collaborative open-source effort, I also welcome feedback and contribution from others.

## Example

```swift
//bfs traversal with inout closure function
func traverse(_ startingv: Vertex, formula: (_ node: inout Vertex) -> ()) {
    //establish a new queue
    let graphQueue: Queue<Vertex> = Queue<Vertex>()
    
    //queue a starting vertex
    graphQueue.enQueue(startingv)
    
    while !graphQueue.isEmpty() {
        //traverse the next queued vertex
        guard var vitem = graphQueue.deQueue() else {
            break
        }
        
        //add unvisited vertices to the queue
        for e in vitem.neighbors {
            if e.neighbor.visited == false {
                print("adding vertex: \(e.neighbor.key) to queue..")
                graphQueue.enQueue(e.neighbor)
            }
        }
        
        //invoke formula
        formula(&vitem)
    } //end while
    
    print("graph traversal complete..")
}
```

## Usage

Individuals are welcome to use the code with commercial and open-source projects. As a courtesy, please provide attribution to [waynewbishop.com](http://www.waynewbishop.com). For more information, review the complete license agreement.

## Questions

Have a question? Feel free to [contact me](https://www.linkedin.com/in/waynebishop/) online.