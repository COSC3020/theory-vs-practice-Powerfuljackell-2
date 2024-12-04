# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  -It is based on pure analysis, that is without external impact. From this assumption, the physical state of the machine can have a misleading effect, as the true time it will take code to run (language agnostic) will vary depending on the system it is running on.
    -To add to this, the specified language will also have an impact on runtime and should be chosen carefully. For example, C runs incredibly quickly in comparison to python, this makes sense as python was written in C. This could be startup times, the time it takes to make and access memory, etc.
  -Human failure, due to a human performing the asymptotic analysis the rate of potential errors increases as the complexity of the algorithm increases. This can lead to a true misinterpretation as the provided analysis does not accurately reflect the run time.
  -Since asymptotic analysis focuses on the performance of the algorithm as the input approaches infinity, it can be misleading as the runtimes of small inputs can vary in performance (for example, O(logn) appears to perform poorly in comparison to both O(n) and O(n^2) at small inputs).
    -This can also apply to the disregard of constants and less complex components during the analysis, as they will have an impact on smaller inputs causing variance in results at smaller inputs misleading the user into thinking their code may be better / worse than it actually is.
  

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.
  -Given that a binary search tree's search best search implementation takes O(logn) I would divide 5 by log(1000) or 5 / 3 the multiply that by log(10000) so (5/3)*4 = 20/3 or 6.66 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  -Machine state: What is the speed of the machine? How quickly can it process the 10,000 elements? If the processor within the machine (for example perhaps an embedded system) is slow or does not possess the same resources as another machine this can result in a long running time.
  -Code inefficiency: Is the language that the algorithm written incompatible with the system? Perhaps a compiler error results in inefficient memory handling that slows down the rate of information retrieval.
  -User error: The written code may have been analyzed correctly but only runs effectively given a specific input size or type. This may contribute to the decrease in speed.
    -In this instance, I assume analysis was performed correctly, but if it was not done correctly that would of course impact the expected performance.

Add your answers to this markdown file.
