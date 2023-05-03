Download Link: https://assignmentchef.com/product/solved-cpts-540-artificial-intelligence-homework-11
<br>
Consider the 3×3 Wumpus world shown below. The goal of this simplified game is to be collocated with the gold (where we get a +1000 reward) and not collocated with the Wumpus or a pit (or we get a -1000 reward). All other states have a reward of -1. As before, the agent starts in [1,1], but has only four possible actions: Up, Down, Left, Right (there is no orientation or turning). Each of these actions always works, although attempting to move into a wall results in the agent not moving. We will use reinforcement learning to solve this problem.







<ol start="1000">

 <li>Compute the utility <em>U(s)</em> of each non-terminal state <em>s</em> given the policy shown above. Note that [1,3], [2,3], [3,3] and [3,1] are terminal states, where U([1,3]) = -1000, U([2,3]) = +1000, U([3,3]) = -1000, and U([3,1]) = -1000. You may assume g = 0.9.</li>

 <li>Using temporal difference Q-learning, compute the Q values for Q([1,1],Right), Q([2,1],Up), Q([2,2],Up), after each of ten executions of the action sequence: Right, Up, Up (starting from [1,1] for each sequence). You may assume a = 0.9, g = 0.9, and all Q values for non-terminal states are initially zero.</li>

</ol>

1

<ol start="2">

 <li>Given the following bigram model, compute the probability of the two sentences below. Show your work.</li>

</ol>

<table width="220">

 <tbody>

  <tr>

   <td width="67"><strong>Word 1 </strong></td>

   <td width="66"><strong>Word 2 </strong></td>

   <td width="87"><strong>Frequency </strong></td>

  </tr>

  <tr>

   <td width="67">the</td>

   <td width="66">player</td>

   <td width="87">2,000</td>

  </tr>

  <tr>

   <td width="67">player</td>

   <td width="66">is</td>

   <td width="87">1,000</td>

  </tr>

  <tr>

   <td width="67">is</td>

   <td width="66">next</td>

   <td width="87">3,000</td>

  </tr>

  <tr>

   <td width="67">next</td>

   <td width="66">to</td>

   <td width="87">4,000</td>

  </tr>

  <tr>

   <td width="67">to</td>

   <td width="66">the</td>

   <td width="87">6,000</td>

  </tr>

  <tr>

   <td width="67">to</td>

   <td width="66">a</td>

   <td width="87">5,000</td>

  </tr>

  <tr>

   <td width="67">the</td>

   <td width="66">gold</td>

   <td width="87">2,000</td>

  </tr>

  <tr>

   <td width="67">a</td>

   <td width="66">pit</td>

   <td width="87">1,000</td>

  </tr>

 </tbody>

</table>




<ol>

 <li>“the player is next to the gold”</li>

 <li>“the player is next to a pit”</li>

</ol>




<ol start="3">

 <li>Suppose we add the following two words to the lexicon on slide 23 of the lecture notes:</li>

</ol>

Noun à player

Adverb à next

Using this augmented lexicon and the grammar on slide 24 of the lecture notes, show all possible parse trees for each of the following sentences. If there is no parse, then show a new grammar rule consisting of only non-terminals that will allow the sentence to be parsed, and show the parse tree.

<ol>

 <li>“the player is next to the gold”</li>

 <li>“the player is next to the gold in 2 3”</li>

 <li>“the player is next to the gold and a pit”.</li>

</ol>




<ol start="4">

 <li><em>CptS 540 Students Only.</em> Repeat problem 2a, but using the bigram model available from <u>ngrams.info</u>. Specifically, download the zip file available from <u>https://www.ngrams.info/iweb/iweb_ngrams_sample.zip</u>. This zip file contains a bigram model in the file “ngrams_words_2.txt”. Use this file to compute the probability for the sentence in problem 2a. Show your work. Note:

  <ul>

   <li>Ignore case in the bigram model, i.e., treat all letters as lowercase. For example, when computing the frequency of “is”, sum the frequencies of all bigrams that begin with “is”, “Is” and “IS”.</li>

   <li>If a bigram appears more than once in the model, then use the sum of all the frequencies for calculating probabilities. For example, “next to” appears eight times in the bigram model (see below). So, you would use the sum 612,358 as the frequency of “next to”.</li>

  </ul></li>

</ol>

568013  next    to      II21                    II22

27837   Next    to      II21                    II22

6403    next    to      II21_MD                 II22_II

4043    next    to      MD                      II

2068    next    to      MD                      TO_II

1508    next    to      MD_II21                 II_II22

1419    next    to      MD                      TO

1067    next    to      II21_MD                 II22_TO

2