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
For the second implementation,  I followed -- as can be seen in "style2.pl" fyle. 

To run the program in the terminal follow the instructions below:

> [!TIP]
> To test it in a terminal you need to go the folder with the file, write "swipl" and then "["style2"].".
> 
> 
> Then put one of following queries and the program should return an outfit based on the restrictions.  
> **Example queries:**  
> For a random outfit
> ````
> ?- recommend_outfit(_, _, _).
> ```` 
> For a specific weather outfit write (hot/cold)
> ````
> ?- recommend_outfit(hot, _, _).
> ````
> For a specific ocasion outfit write (casual/formal/workout)
> ````
> % ?- recommend_outfit(_, casual, _).
> ````
> For a specific ocasion and specific weather outfit write (hot/cold), (casual/formal/workout)
> ````
> % ?- recommend_outfit(hot, casual, _).
> % ?- recommend_outfit(cold, formal, _).
> ````
> 


## Tests
To show that the implemented model works as intended and correctly solves the problem a set of documented tests are shown. 
Looking for outfits fro the following conditions:
1. Weather: Hot, Formality: Workout
2. Weather: Hot, Formality: Casual
3. Weather: Cold, Formality: _
4. Weather: Cold, Formality: Formal
5. Weather: _, Formality: Casual

### Implementation 1

To test the previous cases we have:
1. Weather: Hot, Formality: Workout  
?- outfit_weather_formality(Top, Outerwear, Bottoms, Footwear, hot, workout).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/bfb81379-fac5-4438-905c-0e783595a3f3)
The outfit coresponds.

3. Weather: Hot, Formality: Casual  
?- outfit_weather_formality(Top, Outerwear, Bottoms, Footwear, hot, casual).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/3c14be06-b045-4b33-b5d2-c78a3ec98bcc)
The outfit coresponds.

4. Weather: Cold, Formality: _  
outfit_weather(Top, Outerwear, Bottoms, Footwear, cold).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/19b13f11-bd48-4866-b7af-6047c1c3d0a5)
The outfit coresponds.

5. Weather: Cold, Formality: Formal  
?- outfit_weather_formality(Top, Outerwear, Bottoms, Footwear, cold, formal).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/baabdaa8-4cca-4183-a447-d69e203071c8)
The outfit coresponds.

6. Weather: _, Formality: Casual  
?- outfit_formality(Top, Outerwear, Bottoms, Footwear, casual).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/5acba75c-f3da-4a15-97e8-679670c08579)
The outfit coresponds.

### Implementation 2
To test the previous cases we have:
1. Weather: Hot, Formality: Workout  
?- recommend_outfit(hot, workout, _).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/95e41a6e-ae8d-44c5-b242-22aa061b8e69)
The outfit coresponds.

2. Weather: Hot, Formality: Casual  
?- recommend_outfit(hot, casual, _).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/33b5ce02-0c74-4708-b620-b2141d283a0a)
The outfit coresponds.
3. Weather: Cold, Formality: _  
?- recommend_outfit(cold, _, _).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/59ca7317-a355-4815-bec0-168d3d2845a9)
The outfit coresponds.
4. Weather: Cold, Formality: Formal  
?- recommend_outfit(cold, formal, _).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/eb934a15-b549-4d8e-8609-eb9363bc11fe)

The outfit coresponds.
5. Weather: _, Formality: Casual  
?- recommend_outfit(_, casual, _).
![image](https://github.com/ZValer/Style_Logic/assets/111622587/57593259-7d17-47f7-8aad-3d9a13b623e8)

The outfit coresponds.


## Analysis 
### Implementation 1
The complexity of my model overall is O(n).  

Breaking down the code we can realize that the main predicate is the **outfit_weather_formality** because it combines the other predicates and includes the **no_color_match**.  
- Defining clothing items and attributes are simple facts O(1).
- It calls the no_color_match/2 predicate and since it performs a constant number of comparisons is O(1).

For each combination of tops, outerwear, bottoms and footwear it checks the formality and weather
making it O(n).  
n = tops x outerwear x bottoms xootwear

### Implementation 2
The complexity of my model overall is O(n<sup>4</sup>).   
Breaking it down we have:
**outfit_recommendation/3** 
- the setof/3 predicate is used to collect all clothing items that match the given weather and formality into the Items list. O(n)
- The member/2 predicate is used to generate combinations of tops, bottoms, outerwear, and footwear from the Items list. Which in the worst case s cenario involves (n<sup>4</sup>) combinations. Being the overall time complexity
- no_color_match/4 same as the previous implementation is O(1).

## Conclusion
Some differences are presented in both implementations.
The first one is in the way the clothing items are declared:
Implementation 1:
![image](https://github.com/ZValer/Style_Logic/assets/111622587/d666568a-6d3d-4270-8547-5828c2ceab2f)
Implementation 2:
![image](https://github.com/ZValer/Style_Logic/assets/111622587/80bfb68f-a0bc-478b-bc94-0237672791bc)

Also in the queries. While in implmentation 1 they are different queries for the different especifications:  
- outfit(Top, Outerwear, Bottoms, Footwear).  
- outfit_weather(Top, Outerwear, Bottoms, Footwear, hot).  
- outfit_formality(Top, Outerwear, Bottoms, Footwear, casual).  
- outfit_weather_formality(Top, Outerwear, Bottoms, Footwear, hot, casual).  

For implementation 2 is the same query:
- recommend_outfits(cold, formal, _).  

I consider that in the second implementation it is easier to declare clothing items, it is simpler to consult outfits for the user because it is only one query. However given the time complexity difference, Implementation 1 is the most optimal and a better fit for the solution. 

## References

Lucid Software Inc. (2024). What is a Flowchart. Lucidchart. Retrieved from: https://www.lucidchart.com/pages/what-is-a-flowchart-tutorial 

