Download Link: https://assignmentchef.com/product/solved-csci567-homework-3-kernels
<br>
<h1></h1>

<em>,          </em>if <em>x </em>= <em>x</em><sup>0 </sup><em>,              </em>∀<em>x,</em><em>x</em>0 ∈ R<em>D.           </em>(1) otherwise

<strong>Q1.1 </strong>Prove that this is a valid kernel. You can apply the Mercer’s theorem mentioned in the lectures (lec10.pdf) and assume that the <em>N </em>points {<em>x</em><sub>1</sub><em>,</em>··· <em>,</em><em>x<sub>N</sub></em>} you pick are distinct (i.e., <em>x<sub>i </sub></em>6= <em>x<sub>j </sub></em>if <em>i </em>6= <em>j</em>).

<em>What to submit: </em>No more than 10 lines of proof.

<strong>Q1.2 </strong>Suppose now you are given a training set for a regression problem, where <em>x<sub>i </sub></em>6= <em>x<sub>j </sub></em>if <em>i </em>6= <em>j</em>. Show that by using this kernel, training a kernel ridge regressor (lec10.pdf) with <em>λ </em>= 0 will always lead to the training objective of 0—meaning that all the training examples are <em>predicted accurately </em>by the learned regressor. The training objective of kernel ridge regression is as follows

<em>Kα </em>− <em>y<sup>T </sup></em><em>Kα         </em><em>αKα</em><em>,                                                </em>(2)

where <em>K </em>∈ R<em><sup>N</sup></em><sup>×<em>N </em></sup>is the kernel matrix, <em>y </em>= [<em>y</em><sub>1</sub><em>,y</em><sub>2</sub><em>,</em>··· <em>,y<sub>N</sub></em>]<em><sup>T </sup></em>, and <em>α </em>∈ R<em><sup>N</sup></em>. The learned regressor is

<em>f</em>(<em>x</em>) = [<em>k</em>(<em>x,</em><em>x</em><sub>1</sub>)<em>,k</em>(<em>x,</em><em>x</em><sub>2</sub>)<em>,</em>··· <em>,k</em>(<em>x,</em><em>x<sub>N</sub></em>)]<em>α</em><sup>∗</sup><em>,                                                              </em>(3)

where <em>α</em><sup>∗ </sup>= argmin<em><sub>α </sub>J</em>(<em>α</em>)

<em>What to submit: </em>No more than 5 lines of derivations, plus 1 line to show what <em>α</em><sup>∗ </sup>is.

<strong>Q1.3 </strong>Although the learned regressor can accurately predict the value of each training example, it does not generalize to the test data. Specifically, show that for any <em>x </em>with <em>x </em>6= <em>x<sub>n</sub>,</em>∀<em>n </em>= 1<em>,</em>2<em>,</em>··· <em>,N</em>, the predicted value is always 0.

<em>What to submit: </em>No more than 5 lines of derivations.

<h1>2           Support Vector Machines</h1>

[Recommended maximum time spent: 2 hours]

Consider the dataset consisting of points (<em>x,y</em>), where <em>x </em>is a real value, and <em>y </em>∈ {−1<em>, </em>1} is the class label. Let’s start with three points (<em>x</em><sub>1</sub><em>,y</em><sub>1</sub>) = (−1<em>, </em>−1)<em>, </em>(<em>x</em><sub>3</sub><em>,y</em><sub>3</sub>) = (0<em>, </em>1)<em>, </em>(<em>x</em><sub>2</sub><em>,y</em><sub>2</sub>) = (1<em>,</em>−1).

Figure 1: Three data points considered in Q2

<strong>Q2.1 </strong>Can three points shown in Figure 1, in their current one-dimensional feature space, be perfectly separated with a linear separator? Why or why not?

<em>What to submit: </em>No more than 3 lines of reasoning.

<strong>Q2.2 </strong>Now we define a simple feature mapping <em>φ</em>(<em>x</em>) = [<em>x,x</em><sup>2</sup>]<em><sup>T </sup></em>to transform the three points from one- to two-dimensional feature space. Plot the transformed points in the new two-dimensional feature space (use any package you prefer for the plot, e.g., Matplotlib, PowerPoint). Is there a linear decision boundary that can separate the points in this new feature space? Why or why not? <em>What to submit: </em>The plot and no more than 3 lines of reasoning.

<strong>Q2.3 </strong>Given the feature mapping <em>φ</em>(<em>x</em>) = [<em>x,x</em><sup>2</sup>]<em><sup>T </sup></em>, write down the kernel function <em>k</em>(<em>x,x</em><sup>0</sup>). Moreover, write down the 3 × 3 kernel (or Gram) matrix <em>K </em>based on <em>k</em>(<em>x<sub>i</sub>,x<sub>j</sub></em>) of the three data points. Verify that <em>K </em>is a positive semi-definite (PSD) matrix. You may want to show this by the definition of PSD matrix: a symmetric <em>N </em>×<em>N </em>real matrix <em>M </em>is said to be positive semi-definite if the scalar <em>z<sup>T </sup></em><em>Mz </em>is non-negative for every non-zero column vector <em>z </em>of <em>N </em>real numbers.

<em>What to submit: </em>The form of kernel function <em>k</em>, the kernel matrix <em>K</em>, and no more than 10 lines of proof to show that <em>K </em>is PSD.

<strong>Q2.4 </strong>Now you are going to learn a <em>hard margin </em>SVM classifier on this dataset with <em>k</em>(<em>x<sub>i</sub>,x<sub>j</sub></em>). Recall the primal and dual formulation you learned in lecture 11 (lec11.pdf). Write down the primal and dual formulations of this problem.

<em>What to submit: </em>Primal and dual formulations. Each with no more than 5 lines.

<strong>Q2.5 </strong>Next, you are going to solve this problem using its dual formulation. Recall the toy example we walked through in lecture 12 (lec12.pdf). You may want to borrow a similar symmetric property to simplify the dual formulation.

<em>What to submit: </em>Solve the dual formulation and report the vector <em>α </em>∈ R<sup>3</sup>, the weight vector <em>w </em>∈ R<sup>2 </sup>and the bias <em>b </em>∈ R. No more than 10 lines of derivation.

<strong>Q2.6 </strong>Let ˆ<em>y </em>= <em>w<sup>T </sup>φ</em>(<em>x</em>) + <em>b</em>, where <em>w </em>and <em>b </em>are the weights and the bias you got from the previous question. Draw the decision boundary in the new two-dimensional feature space and circle all support vectors. (Set ˆ<em>y </em>to 0 to get the decision boundary). Then, draw the decision boundary in the original one-dimensional setting.

<em>What to submit: </em>Two plots: one in the new two-dimensional feature space, and the other in the original one-dimensional feature space.

<h1>3           Adaboost for building up a nonlinear classifier</h1>

[Recommended maximum time spent: 2 hour]

In the lectures (lec13.pdf), you learned an algorithm, Adaboost, which constructs a strong (binary) classifier based on iteratively adding one weak (binary) classifier into it. A weak classifier is learned to maximize the <em>weighted training accuracy </em>at the corresponding iteration, and the weight of each training example is updated after every iteration. Algorithm 1 summarizes the algorithm of Adaboost.

<strong>Given</strong>

H: A set of functions, where <em>h </em>∈ H takes a <em>D</em>-dimensional vector as input and outputs either +1 or −1.

A training set.

<strong>Goal </strong>Learn       )], where <em>f<sub>t </sub></em>∈ H and <em>β<sub>t </sub></em>∈ R.

<strong>Initialization </strong><em>w</em><sub>1</sub>(<em>n</em>) = <em><sub>N</sub></em><u><sup>1 </sup></u><em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>··· <em>,N</em>}.

<strong>for </strong><em>t </em>= 1<em>,</em>2<em>,</em>··· <em>,T </em><strong>do</strong>

<ul>

 <li>find <em>f<sub>t </sub></em>= argmin<em><sub>h</sub></em><sub>∈H </sub><sup>P</sup><em><sub>n </sub>w<sub>t</sub></em>(<em>n</em>)I[<em>y<sub>n </sub></em>6= <em>h</em>(<em>x<sub>n</sub></em>)]</li>

 <li>compute</li>

</ul>

<em> </em>(c) compute

<em>t</em>

(

<em>w<sub>t</sub></em>(<em>n</em>)exp(−<em>β<sub>t</sub></em>)<em>,           </em>if <em>y<sub>n </sub></em>= <em>f<sub>t</sub></em>(<em>x<sub>n</sub></em>)

<ul>

 <li>compute <em>w<sub>t</sub></em><sub>+1</sub>(<em>n</em>) = <em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>·· <em>,N</em>}</li>

</ul>

<em>w<sub>t</sub></em>(<em>n</em>)exp(<em>β<sub>t</sub></em>)<em>,           </em>otherwise

<ul>

 <li>normalize<strong>end</strong></li>

</ul>

<strong>Algorithm 1: </strong>The Adaboost algorithm

Figure 2: The two training sets considered in Q3: (A) for Q3.1, Q3.2, and (B) for Q3.3, Q3.4, Q3.5, Q3.6.

In this question, you are going to experiment with the learning process of Adaboost, with decision stumps as H. A decision stump <em>h </em>∈ H is a classifier characterized by a triplet (<em>s </em>∈ {+1<em>,</em>−1}<em>,b </em>∈ R<em>,d </em>∈ {1<em>,</em>2<em>,</em>··· <em>,D</em>}) such that

( <em>s,       </em>if <em>x<sub>d </sub>&gt; b,</em>

<em>h</em>(<em>s,b,d</em>)(<em>x</em>) =                                                                                                          (4)

−<em>s,     </em>otherwise<em>.</em>

That is, each decision stump function only looks at a single dimension/entry <em>x<sub>d </sub></em>of the input vector <em>x</em>, and check whether <em>x<sub>d </sub></em>is larger than <em>b </em>or not (<em>s </em>decides which label to give if <em>x<sub>d </sub>&gt; b</em>).

Specifically, you are given a simple 4-example training set (as illustrated in Fig. 2 (A)):

For simplicity, let’s consider

H = {<em>h</em><sub>(<em>s,b,d</em>) </sub>| <em>s </em>∈ {+1<em>,</em>−1}<em>,b </em>∈ {−2<em>,</em>−0<em>.</em>5<em>,</em>0<em>.</em>5<em>,</em>2}<em>,d </em>∈ {1<em>,</em>2}}<em>.                                           </em>(5)

That is, H contains only 16 distinct decision stump functions (8 horizontal boundaries and 8 vertical boundaries).

<strong>Q3.1 </strong>Let’s get started to run Adaboost for <em>T </em>= 3. At <em>t </em>= 1, please find the best decision stump <em>f</em><sub>1 </sub>(i.e., solve step (a) in Algorithm 1). If there are multiple equally best stump functions, just randomly pick <strong>ONE </strong>of them to be <em>f</em><sub>1</sub>. What are the corresponding based on <em>f</em><sub>1</sub>?

<em>What to submit: </em>Write down the triplet (<em>s,b,d</em>) of <em>f</em><sub>1</sub>, and the values of . Please round your results to two decimal places (e.g., 1.499 becomes 1.50).

<strong>Q3.2 </strong>From your results in Q3.1 and Algorithm 1, you will observe something interesting about Adaboost. That is, if <em>β<sub>t </sub></em>= 0, the corresponding iteration <em>t </em>does not contribute anything to the final decision function <em>F</em>(<em>x</em>). This might be fine since we can move on to the next iteration and probably get <em>β<sub>t</sub></em><sub>+1 </sub>6= 0 there. Let’s have a try. Please write down <em>w</em><sub>2</sub>(<em>n</em>)<em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>··· <em>,N</em>}, and check the objective function to solve at <em>t </em>= 2 (i.e., solve step (a) in Algorithm 1). You will observe that the objective function at <em>t </em>= 2 remains exactly the <strong>SAME </strong>as at <em>t </em>= 1. The Adaboost algorithm thus will likely get stuck after iteration <em>t </em>= 1.

<em>What to submit: </em>Write down <em>w</em><sub>2</sub>(<em>n</em>)<em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>3<em>,</em>4}. Please round your results to two decimal places (e.g., 1.499 becomes 1.50).

<strong>Q3.3 </strong>From the observations in Q3.2, it seems like Adaboost is not really learning something <em>strong</em>. We argue that it is because of the form of decision stumps: each of them can only draw a horizontal or vertical decision boundary in our 2-dimensional case. Can we do any simple trick to solve this issue?

Let’s try one trick that you have learned, feature transform. Specifically, we apply a simple linear transformation for every example

<em>x</em><em>,                                                                             </em>(6)

which results in a transformed training set

<em>.</em>

From now on, let’s only consider this new training set (as illustrated in Fig. 2 (B)), but use the same H defined in eq. (5).

Let’s get started again to run Adaboost for <em>T </em>= 3, using the new training set. At <em>t </em>= 1, please find the best decision stump <em>f</em><sub>1 </sub>(i.e., solve step (a) in Algorithm 1). If there are multiple equally best stump functions, just randomly pick <strong>ONE </strong>of them to be <em>f</em><sub>1</sub>. What are the corresponding <sub>1 </sub>and <em>β</em><sub>1 </sub>based on <em>f</em><sub>1</sub>?

<em>What to submit: </em>Write down the triplet (<em>s,b,d</em>) of <em>f</em><sub>1</sub>, and the values of . Please round your results to two decimal places (e.g., 1.499 becomes 1.50).

<strong>Q3.4 </strong>Now you should see that Adaboost does learn something at <em>t </em>= 1 (i.e., <em>β</em><sub>1 </sub>6= 0). Let’s move on to <em>t </em>= 2. Please first write down <em>w</em><sub>2</sub>(<em>n</em>)<em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>3<em>,</em>4} for each example. Then, please find the best decision stump <em>f</em><sub>2 </sub>(i.e., solve step (a) in Algorithm 1). If there are multiple equally best stump functions, just randomly pick <strong>ONE </strong>of them to be <em>f</em><sub>2</sub>. What are the corresponding <sub>2 </sub>and <em>β</em><sub>2 </sub>based on <em>f</em><sub>2</sub>?

<em>What to submit: </em>Write down <em>w</em><sub>2</sub>(<em>n</em>)<em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>3<em>,</em>4}, the triplet (<em>s,b,d</em>) of <em>f</em><sub>2</sub>, and the values of. Please round your results to two decimal places (e.g., 1.499 becomes 1.50).

<strong>Q3.5 </strong>Let’s move on to <em>t </em>= 3. Please first write down <em>w</em><sub>3</sub>(<em>n</em>)<em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>3<em>,</em>4} for each example. Then, please find the best decision stump <em>f</em><sub>3 </sub>(i.e., solve step (a) in Algorithm 1). If there are multiple equally best stump functions, just randomly pick <strong>ONE </strong>of them to be <em>f</em><sub>3</sub>. What are the corresponding based on <em>f</em><sub>3</sub>?

<em>What to submit: </em>Write down <em>w</em><sub>3</sub>(<em>n</em>)<em>,</em>∀<em>n </em>∈ {1<em>,</em>2<em>,</em>3<em>,</em>4}, the triplet (<em>s,b,d</em>) of <em>f</em><sub>3</sub>, and the values of. Please round your results to two decimal places (e.g., 1.499 becomes 1.50).

<strong>Q3.6 </strong>Please combine your results of Q3.3, Q3.4, and Q3.5, and write down your learned <em>F</em>(<em>x</em>) in terms of <em>h</em><sub>(<em>s,b,d</em>)</sub>, <em>β</em><sub>1</sub>, <em>β</em><sub>2</sub>, and <em>β</em><sub>3</sub>. You should plug <strong>VALUES </strong>into <em>s,b,d,β</em><sub>1</sub><em>,β</em><sub>2</sub><em>,β</em><sub>3</sub>. For example,

<em>F</em>(<em>x</em>) = sign[0<em>.</em>5 × <em>h</em><sub>(+1<em>,</em>0<em>.</em>5<em>,</em>1)</sub>(<em>x</em>) + 0<em>.</em>5 × <em>h</em><sub>(</sub>−<sub>1<em>,</em>0<em>.</em>5<em>,</em>1)</sub>(<em>x</em>) + 0<em>.</em>5 × <em>h</em><sub>(</sub>−<sub>1<em>,</em>2<em>,</em>2)</sub>(<em>x</em>)]. Then please write down the predicted labels of <em>x</em><sub>1</sub><em>,</em><em>x</em><sub>2</sub><em>,</em><em>x</em><sub>3</sub><em>,</em><em>x</em><sub>4 </sub>using <em>F</em>(<em>x</em>). How many training examples are correctly labeled by <em>F</em>(<em>x</em>)?

<em>What to submit: </em>Write down <em>F</em>(<em>x</em>), and compute <em>F</em>(<em>x</em><sub>1</sub>)<em>,F</em>(<em>x</em><sub>2</sub>)<em>,F</em>(<em>x</em><sub>3</sub>)<em>,F</em>(<em>x</em><sub>4</sub>), and the number of correctly labeled examples. Please round your results to two decimal places (e.g., 1.499 becomes 1.50).

<strong>Q3.7 </strong>From Q3.6, you should see that Adaboost with decision stumps can solve a problem similar to XOR in 3 iterations, by using a simple linear transformation (more precisely, 2-dimensional rotation). Note that the decision boundary by <em>F</em>(<em>x</em>) is nonlinear, even though that <em>h </em>∈ H can only produce a linear boundary. Also note that, even with the same feature transform, a linear classifier such as logistic regression cannot correctly label every training example in our case.

<em>What to submit: </em>Nothing.

<strong>Programming component</strong>

<h1>4           High-level descriptions</h1>

<h2>4.1         Dataset</h2>

We will use <strong>mnist subset </strong>(images of handwritten digits from 0 to 9). This is the same subset of the full MNIST that we used for Homework 1 and Homework 2. As before, the dataset is stored in a JSON-formated file <strong>mnist subset.json</strong>. You can access its training, validation, and test splits using the keys ‘train’, ‘valid’, and ‘test’, respectively. For example, suppose we load <strong>mnist subset.json </strong>to the variable <em>x</em>. Then, <em>x</em>[<sup>0</sup><em>train</em><sup>0</sup>] refers to the training set of <strong>mnist subset</strong>. This set is a list with two elements: <em>x</em>[<sup>0</sup><em>train</em><sup>0</sup>][0] containing the features of size <em>N </em>(samples) ×<em>D </em>(dimension of features), and <em>x</em>[<sup>0</sup><em>train</em><sup>0</sup>][1] containing the corresponding labels of size <em>N</em>.

<h2>4.2         Tasks</h2>

You will be asked to implement the linear support vector machine (SVM) for binary classification

(Sect. 5). Specifically, you will

<ul>

 <li>finish implementing the following three functions—objective function, pegasos train, and pegasos test—in py. Refer to pegasos.py and Sect. 5 for more information.</li>

 <li>Run the script sh after you finish your implementation. This will output pegasos.json.</li>

 <li>add, commit, and push (1) the py, and (2) the pegasos.json file that you have created.</li>

</ul>

As in the previous homework, you are not responsible for loading/pre-processing data; we have done that for you (e.g., we have pre-processed the data to have to class: digits 0–4 and digits 5–9.). For specific instructions, please refer to text in Sect. 5 and the instructions in pegasos.py.

<h2>4.3         Cautions</h2>

Please do not import packages that are not listed in the provided code. Follow the instructions in each section strictly to code up your solutions. <strong>Do not change the output format</strong>. <strong>Do not modify the code unless we instruct you to do so</strong>. A homework solution that does not match the provided setup, such as format, name, initializations, etc., <strong>will not </strong>be graded. It is your responsibility to <strong>make sure that your code runs with the provided commands and scripts on the VM</strong>. Finally, make sure that you <strong>git add, commit, and push all the required files</strong>, including your code and generated output files.

<h1>5           Pegasos: a stochastic gradient based solver for linear SVM</h1>

In this question, you will build a linear SVM classifier using the Pegasos algorithm [1]. Given a

training set, the primal formulation of linear SVM is as follows

<em>λ</em>

<em>                  </em><em>                                                    .                                                     </em>(7)

Instead of turning it into dual formulation, we are going to solve the primal formulation directly with a gradient-base algorithm. <em>Note that here we include the bias term b into parameter </em><em>w by appending </em><em>x with </em>1<em>.</em>

In (batch) gradient descent, at each iteration of parameter update, we compute the gradients for all data points and take the average (or sum). When the training set is large (i.e., <em>N </em>is a large number), this is often too computationally expensive (for example, a too large chunk of data cannot be held in memory). Stochastic gradient descent with mini-batch alleviates this issue by computing the gradient on a <em>subset </em>of the data at each iteration.

One key issue of using (stochastic) gradient descent to solve eq. (7) is that max{0<em>,z</em>} is not differentiable at <em>z </em>= 0. You have seen this issue in Homework 2, where we use the Heaviside function to deal with it. In this question, you are going to learn and implement Pegasos, a representative solver of eq. (7) that applies stochastic gradient descent with mini-batch and explicitly takes care of the non-differentiable issue.

The pseudocode of Pegasos is given in Algorithm 2. At the <em>t</em>-th iteration of parameter update, we first take a mini-batch of data <em>A<sub>t </sub></em>of size <em>K </em>[step (a)], and define <em>A</em><sup>+</sup><em><sub>t </sub></em>⊂ <em>A<sub>t </sub></em>to be the subset of samples for which <em>w<sub>t </sub></em>suffers a non-zero loss [step (b)]. Next we set the learning rate <em>η<sub>t </sub></em>= 1<em>/</em>(<em>λt</em>) [step (c)]. We then perform a <strong>two-step parameter update </strong>as follows. We first compute (1−<em>η<sub>t</sub>λ</em>)<em>w<sub>t </sub></em>and for all samples (<em>x,y</em>) ∈ <em>A</em><sup>+</sup><em><sub>t </sub></em>we add the vector <em>x </em>to (1−<em>η<sub>t</sub>λ</em>)<em>w<sub>t</sub></em>. We denote the resulting vector by <em>w </em> [step (d)]. This step can also be written as <em>w<sub>t</sub></em><sub>+</sub><u>1 </u>= <em>w<sub>t </sub></em>− <em>η<sub>t</sub></em>∇<em><sub>t </sub></em>where

2

<em>x</em>

The definition of the hinge loss, together with the Heaviside function, implies that ∇<em><sub>t </sub></em>is the gradient of the objective function on the mini-batch <em>A<sub>t </sub></em>at <em>w<sub>t</sub></em>. Last, we set <em>w<sub>t</sub></em><sub>+1 </sub>to be the projection of <em>w<sub>t</sub></em><sub>+</sub><u>1 </u>onto the set

2

√

<em>B </em>= {<em>w </em>: ||<em>w</em>|| ≤ 1<em>/ λ</em>}

√

1<em>/ λ</em>

This is obtained by scaling <em>w<sub>t</sub></em><sub>+1 </sub>by min{1<em>,</em>} [step (e)]. For details of Pegasos algorithm you may refer to the original paper [1].

<strong>Input </strong>A training set, the total number of iterations <em>T</em>, the batch size <em>K</em>, and the regularization parameter <em>λ</em>.

<strong>Output </strong>The last weight <em>w<sub>T</sub></em><sub>+1</sub>.

<strong>Initialization </strong>Choose <em>w</em><sub>1 </sub>s.t. .

<strong>Algorithm 2: </strong>The Pegasos algorithm

Now you are going to implement Pegasos and train a binary linear SVM classifier on the dataset <strong>mnist subset.json</strong>. You are going to implement three functions—objective function, pegasos train, and pegasos test—in a script named pegasos.py. You will find detailed programming instructions in the script.

<strong>Q5.1      </strong>Finish the implementation of the function objective function, which corresponds to the objective function in the primal formulation of SVM.

<strong>Q5.2          </strong>Finish the implementation of the function pegasos train, which corresponds to Algorithm

2.

<strong>Q5.3 </strong>After you train your model, run your classifier on the test set and report the accuracy, which is defined as:

# of correctly classified test samples

# of test samples

Finish the implementation of the function pegasos test.

<strong>Q5.4 </strong>After you complete above steps, run pegasos.sh, which will run the Pegasos algorithm for 500 iterations with 6 settings (mini-batch size <em>K </em>= 100 with different <em>λ </em>∈ {0<em>.</em>01<em>,</em>0<em>.</em>1<em>,</em>1} and <em>λ </em>= 0<em>.</em>1 with different <em>K </em>∈ {1<em>,</em>10<em>,</em>1000}), and output a pegasos.json that records the test accuracy and the value of objective function at each iteration during the training process.

<em>What to do and submit: </em>run script pegasos.sh. It will generate pegasos.json. Add, commit, and push both pegasos.py and pegasos.json before the due date.

<strong>Q5.5     </strong>Based on pegasos.json, you are encouraged to make plots of the objective function value versus the number of iterations (i.e., a convergence curve) in different settings of <em>λ </em>and <em>k</em>, but you are not required to submit these plots.