GSoC 2015 Enhanced vector and deque containers Proposal
Personal Details
•	Name: Yingjie Liu
•	University: Northwestern Polytechnical University
•	Course/Major: Software Engineer
•	Degree Program: B.Sc.
•	Email: 18706819589@163.com
•	Homepage: 
•	Availability: I'd like to spend 35 to 40 hours every week on GSoC. In July and August, I will spend more time on GSoC. After September, I will spend 20 hours every week on GSoC.
Background Information
Please summarize your educational background (degrees earned, courses taken, etc.). Please summarize your programming background (OSS projects, internships, jobs, etc.).
I'm a Software Engineer B.Sc student and I have studied most of the programming courses such as, C++, Java, Data Structure and Algorithms, Database, Network and so on. I like programming by using C and C++. I usually delve into data structure and algorithms, practicing them by programming in Online Judging. As for my project, I have finished one about Data Mining using python and the Machine Learning library Scikit-learn. I haven’t upload my project to GitHub, because it was total finished several days ago.
Please tell us a little about your programming interests.
C++ is my favorite programming language. I am interested in STL, and I read the source code of STL, including, Allocator, Iterator, Sequence Container, Associative Containers, Algorithms and others. I am also familiar with Boost.
Please tell us why you are interested in contributing to the Boost C++ Libraries.
I learned about Boost about 1 year ago, which is the pre-standard C ++ library, then I tried to use Boost in my program, and I was surprised at its powerful functions. I also used Boost libraries (such as Boost MPI) in some contests, and its performance make my teammates and me satisfied. I'd like to grab the opportunity of GSoC '15 and contribute my efforts to Boost, to make Boost be stronger.
What is your interest in the project you are proposing?
I think the standard containers std::vector and std::deque should be strengthened, for example, some functions can be added, algorithms can be changed to be better, and some exceptions should be handled. I’d like to strengthen vector and deque to make them perfect. 
Have you done any previous work in this area before or on similar projects?
I have programmed some small containers like vector before, and the container can handle some exceptions such as iterator is beyond the size.
What are your plans beyond this Summer of Code time frame for your proposed work?.
I will talk with others and change the bugs they found or add some new functions to the container.
Please rate, from 0 to 5 (0 being no experience, 5 being expert), your knowledge of the following languages, technologies, or tools:
The following are rated as a skills of a student:
•	C++ 98/03: 2, I used it about 2 year ago.
•	C++ 11/14: 4, This is the main C++ standard I am using.
•	C++ Standard Library: 5, I think I know the source code of STL better.
•	Boost C++ Libraries: 2, I used some libraries of Boost(MPI), and I am familiar with some famous Boost libraries.
•	Git: 2, I just know about it, but I haven’t used it.
What software development environments are you most familiar with (Visual Studio, Eclipse, KDevelop, etc.)?
Visual Studio and CodeBlocks are the software development environments I most familiar with

Project Proposal
I agree to “write a full-fledged and enhanced C++11 versions of std::vector and std::deque with extra functionality that gives the programmer more control over buffers, segments and iteration” as described in the Boost GSoC Page.
I think the algorithms for some operations such as push_front, pop_front, push_back and pop_back can be optimized to O(1) time by changing the start or finish iterator. In the same time, the exception caused in memory should be handled.
For deque, I think the buffers, segments and iteration can be optimized, and the specialized way can be talked later.

Proposed Milestones and Schedule
I think the are: realize the interface, create an initial implementation and tests, then adjust the algorithms to optimize, do unit test and focus on the details.
The planned schedule is:
•	Weeks 1, 2: Studying the source code of vector and deque in deep, and write down the basic plans for the new vector and deque
•	Weeks 3, 4, 5: Finish the first version of new Vector, and test it.
•	Weeks 6, 7, 8: Finish the first version of new Deque, and test it.
•	Weeks 9,10,12: Optimize the algorithms of new Vector and Deque. Make them perfect in details and fix the bugs.
•	Weeks 13….: Maintain the new Vector and Deque
Programming Competency
I have written a small vector-like C++11 container as described in the Boost GsoC Page. Here are the main functions and some details of it(in myVec.cpp):
(1) Functions begin(), end() return the start and finish iterator (I use pointer to be Iterator).
(2) Functions size(), capacity() return the real size and the capacity of the container.
(3) Function empty() return a bool about whether the container is empty.
(4) Function operator[](size_type n) is an overload function about the operator [ ]
(5) Function myVec(size_type n, const T& value) is one of the constructors.
(6) Function push_back(const T& x) adds a new element to the end, and it will double the capacity if it’s full.
(7) Function pop_back() deletes the last element of the container
(8) Function erase(iterator position) erases the element.
(9) Function erase(iterator first, iterator last) erases the elements from first to last but not include last.
(10) Function insert(iterator pos, const T& x) inserts an element x in the position behind the iterator pos.
(11) Function resize(size_type new_size, const T& x) create a new size of container and fill the empty place with x.
(12) Function clear() clears the container.
