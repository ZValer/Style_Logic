# Style_Logic

# E4 Demonstration of a Programming Paradigm

## Description 
**Context of the problem and programming paradigm.**


Fashion is all around us. Since the moment we prepare ourselves to leave the house we have to choose what to wear. The selection is a representation of ourselves and what we want to show the world about us. The fashion industry is huge and has a big impact on what we wear and how we feel.   

This industry is embracing technology in various ways to innovate and improve the design, production, and consumption of clothing and accessories. E-commerce platforms, mobile apps and programs have improved their sales and the way they interact in various ways with the consumers. This helps people get more involved in the fashion industry by making it easier to learn and create. 

Imagine a program that helps you pick out outfits based on things like the weather, the colors you like, and where you're going. It could make getting dressed in the morning a whole lot easier and more fun, making fashion more accessible and enjoyable for everyone.  

 **How the Logic Paradigm would be used.**
A program can be effectively implemented using the **logic programming paradigm**. Logic programming, supported by languages such as Prolog, revolves around defining rules and facts that the system uses to infer conclusions. For this program, we can define facts and rules about the user's wardrobe items and their characteristics (type, color, weather, formality). We can also define rules of non-matching colors to exclude or rules that dictate suitable outfit combinations based on the weather and event types. With this program then queries can be done to generate suitable outfits, ensuring they meet all the specified criteria. This approach takes advantage of the benefits of logic programming by managing complex decision-making processes and rule-based reasoning, making it suitable for creating a personalized outfit recommendation system.

## Model of the Solution
**The logic of my solution in a diagram**

A flowchart portrays a process, system or computer algorithm. This model is a visual representation of data flow and they are useful to spell out the **logic** behind a program before even starting to code the automated process. They are mostly used to describe processes in a way that is clear and easy-to-understand. Flowcharts use rectangles, ovals, diamonds and other shapes to define the type of step, along with connecting arrows to define flow and sequence.  (Lucid Software Inc, 2024).

![styleflow drawio](https://github.com/ZValer/Style_Logic/assets/111622587/aba4b9b4-89a1-4807-b93c-9e01181d1581)


Let´s break down the model:
The steps are connected through *flow arrows*.   
Some *comments/annotations* were also made to specify a couple of steps.   
The squares represent *processes* as for the diamonds they represent *decisions*. (Lucid Software Inc, 2024). As you can be seen in the diagram, processes follow the flow go to next step while decisions can take different paths depending on the case presented.   
This way the sequential flow of steps of the algorithm is represented in the model. 
 
Following the model, for the implementation the next instructions where applied:
First:  
1. Declare facts about available clothing items with their characteristics (type, color, weather, formality).
Then:
2. Formulate queries based on user input. The queries will request specific outfits with diferent combinations (weather/formality)
3. Define rules for how to combine different clothing items. These rules will guide the decision-making process, ensuring that the recommended outfits meet user preferences and specifications.
4. Generate Outfit Recommendations that fit the user's request and check if the colors of each item combine. If they do go to the next step (5), if not return to (4)
5. Display the recommended outfits to the user.


## Implementation
Implement your solution in a language that supports the programming paradigm.

### Implementation 1
For the first implementation, I followed the model as can be seen "style.pl" fyle. 

To run the program in the terminal follow the instructions below:

> [!TIP]
> To test it in a terminal you need to go the folder with the file, write "swipl" and then "["style"].".
> 
> 
> Then put one of following queries and the program should return an outfit based on the restrictions.  
> **Example queries:**  
> For a random outfit
> ````
> ?- outfit(Top, Outerwear, Bottoms, Footwear).
> ```` 
> For a specific weather outfit write (hot/cold)
> ````
> ?- outfit_weather(Top, Outerwear, Bottoms, Footwear, hot).
> ````
> For a specific ocasion outfit write (casual/formal/workout)
> ````
> % ?- outfit_formality(Top, Outerwear, Bottoms, Footwear, casual).
> ````
> For a specific ocasion and specific weather outfit write (hot/cold), (casual/formal/workout)
> ````
> % ?- outfit_weather_formality(Top, Outerwear, Bottoms, Footwear, hot, casual).
> ````
> 
### Implementation 2
For the second implementation,  I followed -- as can be seen "x.pl" fyle. 

To run the program in the terminal follow the instructions below:

> [!TIP]
> To test it in a terminal you need to go the folder with the file, write "python x.py".
> 
>Then put the query and the program should return ---
>
> 

## Tests

To show that the implemented model works as intended and correctly solves the problem a set of documented tests are shown. 

### Regular Expression

The file "x.py" contains test cases for the x
> [!TIP]
>To test it in a terminal you need to go the folder with the file, write "pyhton test_x.py".

image   

## Analysis 
### Regular Expression
The complexity of my model is in general ---

...

## Conclusion

...   


## References

Lucid Software Inc. (2024). What is a Flowchart. Lucidchart. Retrieved from: https://www.lucidchart.com/pages/what-is-a-flowchart-tutorial 

