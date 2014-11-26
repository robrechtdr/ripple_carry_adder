ripple_carry_adder
==================
> An example of how an abstract operation (addition) can be implemented in a physical system.

The following shows a sequence of additions performed by a *2-bit input based ripple-carry adder (full ripple adder)*. Per step in the sequence one of the operands is increased by one such that the result shows a binary count from 0 up and until 100.

  ![gif](https://raw.github.com/RobrechtDR/ripple_carry_adder/master/.misc/two_bit_input_ripple_carry_adder.gif)
> The two large images at the bottom represent the respective boxes in the middle of the ripple-carry adder in the top left image.

Click on the image to see it enlarged. Also see the following: 

* [Controllable gif](http://gifctrl.com/k8e)
* [Video](https://raw.githubusercontent.com/robrechtdr/ripple_carry_adder/master/.misc/two_bit_input_ripple_carry_adder.mp4)


### What is this thing?

The ripple-carry adder is a particular type of design of the component of a computer that enables it to perform addition.

The 0 and 1 signals per binary digit from x and y are physically implemented by the respective absence and presence of an electric current.

The AND, OR and XOR gates are called logical gates. These are abstractions that can be implemented in the real world using electronic components. It is useful to use abstractions because we want to be able to decouple these concepts from a specific implementation. For one because there are multiple ways these logical gates can be physically implemented.

To find out more about these logical gates and how they can be physically implemented, see [here](http://en.wikipedia.org/wiki/Logic_gate).

To get an idea how the ripple-carry adder fits into the design of a computer, see [here](http://www.cs.hmc.edu/csforall/ComputerOrganization/ComputerOrganization.html#logic-using-electrical-circuits).


### States in the sequence

* **State 0**

  | x | y | x + y  |
  |---|---|--------|
  | 0 | 0 |   0    |

  ![gif](https://raw.github.com/RobrechtDR/ripple_carry_adder/master/.misc/tbirca_state_0.png)


* **State 1**

  | x | y | x + y  |
  |---|---|--------|
  | 0 | 1 |   1    |

  ![gif](https://raw.github.com/RobrechtDR/ripple_carry_adder/master/.misc/tbirca_state_1.png)


* **State 2**

  | x | y | x + y  |
  |---|---|--------|
  | 1 | 1 |   10   |

  ![gif](https://raw.github.com/RobrechtDR/ripple_carry_adder/master/.misc/tbirca_state_2.png)


* **State 3**

  | x | y  | x + y  |
  |---|----|--------|
  | 1 | 10 |   11   |

  ![gif](https://raw.github.com/RobrechtDR/ripple_carry_adder/master/.misc/tbirca_state_3.png)


* **State 4**

  | x | y  | x + y  |
  |---|----|--------|
  | 1 | 11 |   100  |

  ![gif](https://raw.github.com/RobrechtDR/ripple_carry_adder/master/.misc/tbirca_state_4.png)


### Tools used to create the sequence

* logisim (to implement logical circuits)
* shutter (to take screenshots)
* gimp (to compose shots in one image)
* convert (for gif creation)
* kazam (for video creation)
