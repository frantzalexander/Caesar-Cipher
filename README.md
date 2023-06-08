# Caesar-Cipher
Welcome to the Caesar Cipher Project

The project is meant to build a tool that is capable of encrypting and decrypting messages. 

## Key Objectives
* Encode and decode a message.
* The message may consist of more than one word and include numbers.

## The Results
When the program function activates, a display of the ascii art logo for the program title would be shown.  


Afterwards, the program first asks the user for the direction: to either encode and decode. 

Then it asks for the message and amount to shift the characters. 

Additionally, the program incorporates the capacity to encrypt special characters and digits.

Finally, the program would ask if the user would like to continue encoding or decoding messages.


The Graphic User Interface:


![Ceasar Cipher UI](https://github.com/frantzalexander/Caesar-Cipher/assets/128331579/b452fb76-df66-4f97-8c68-1d0915026cfa)

## The Process
```mermaid
flowchart TD
    start(((Start)))
    display[Display the logo]
    generate_list[Generate a list of characters]
    ask1[Ask the user to encode or decode]
    ask2[Ask the user to enter the message]
    ask3[Ask the user the shift amount]
    shift1{Is the shift amount > 26?}
    shift2{{Divide the amount by 26 and shift by the remainder}}
    shift3{{Shift by the given amount}}
    direction1{Is the user asking to decode?}
    direction2{{Multiply shift amount by -1}}
    direction3{{Enter user specified amount}}
    generate_list2[Generate a list of the shifted characters]
    generate_list3[Display encrypted or decrypted message]
    continue{Ask user to continue?}
    finish(((End)))
    start --> display
    display --> generate_list
    generate_list --> ask1
    ask1 --> ask2
    ask2 --> ask3
    ask3 --> shift1
    shift1-->|Yes|shift2
    shift1-->|No|shift3
    shift2 --> direction1
    shift3 --> direction1
    direction1-->|Yes|direction2
    direction1-->|No|direction3
    direction2 --> generate_list2
    direction3 --> generate_list2
    generate_list2 --> generate_list3
    generate_list3 --> continue
    continue -->|Yes|ask1
    continue -->|No|finish
```
