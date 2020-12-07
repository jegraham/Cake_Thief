# Cake_Thief

Inspiration "Cake Thief" https://www.interviewcake.com/question/java/cake-thief?course=fc1&section=dynamic-programming-recursion


You are a renowned thief who has recently switched from stealing precious metals to stealing cakes because of the insane profit margins. You end up hitting the jackpot, breaking into the world's largest privately owned stock of cakes—the vault of the Queen of England.

While Queen Elizabeth has a limited number of types of cake, she has an unlimited supply of each type.

Each type of cake has a weight and a value, stored in objects of a CakeType class:

  public class CakeType {

    final int weight;
    final int value;

    public CakeType(int weight, int value) {
        this.weight = weight;
        this.value  = value;
    }
}
Java
For example:

  // weighs 7 kilograms and has a value of 160 shillings
new CakeType(7, 160);

// weighs 3 kilograms and has a value of 90 shillings
new CakeType(3, 90);

Java
You brought a duffel bag that can hold limited weight, and you want to make off with the most valuable haul possible.

Write a method maxDuffelBagValue() that takes an array of cake type objects and a weight capacity, and returns the maximum monetary value the duffel bag can hold.

For example:

  CakeType[] cakeTypes = new CakeType[] {
    new CakeType(7, 160),
    new CakeType(3, 90),
    new CakeType(2, 15),
};

int capacity = 20;

maxDuffelBagValue(cakeTypes, capacity);
// returns 555 (6 of the middle type of cake and 1 of the last type of cake)

Java
Weights and values may be any non-negative integer. Yes, it's weird to think about cakes that weigh nothing or duffel bags that can't hold anything. But we're not just super mastermind criminals—we're also meticulous about keeping our algorithms flexible and comprehensive.


Questions
---------------------
- Is it possible to have a negative number?
- Is it possible to have an unlimited knapsack or zero cake weight?

Assumptions
---------------------
- maxDuffelBagValue(cakeTypes, capacity);
- positive numbers only
- Sorted high to low


Solutions 
---------------------
- We can iterate through and find the maximum amounts for each cake. This doesnt consider combinations of cakes.

- We can find the cakes with the highest ratios and work our way dwown from the highest ratios. This would be approximately O(n) for time and O(n) for space 

- Dynamic programming or knapsack problem is another application to use to solve this. Let's do this one as we will have the most accurate 

Testcase
---------------------
- negatives 
- 0's
- unlimited size 






