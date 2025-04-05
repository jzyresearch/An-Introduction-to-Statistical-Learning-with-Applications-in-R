# Errata of ISL with Python

记录An Introduction to Statistical Learning with Applications in Python一书的勘误，来源于书籍官网的[Errata](https://www.statlearning.com/errata-python-edition)

## **Since the 1st printing (Summer 2023)**

On page 44, “Out\[22]:” should not be numbered. _The authors._

On page 49, the input block after “In\[43]:” should be numbered (this will affect the numbering of downstream input blocks as well). _The authors._

On the bottom of page 50 of the Chapter 2 lab, the sentence “To fine-tune the output of the ax.contour() function, take a look at the help file by typing ?plt.contour” should instead say “To fine-tune the output of the ax.contour() function, take a look at the help file by typing ?ax.contour” _Thanks to Hargen Zheng._

On page 54, last line above the third code cell: "TRUE" should be "True". _Thanks to Pedro Zühlke._

On page 59, in the last line before the second code cell, there is a repeated “of” in “attribute of of the dataframe”. _Thanks to Pedro Zühlke._

On page 61, block 103, there should be a semi-colon in the last line to indicate that the output should be suppressed. Also, the semi-colon in the first line is superfluous, and should be removed. _Thanks to Julien Gomes._

On page 65, “Its because they are different…” should say “It’s because they are different.” _Thanks to Pedro Zühlke._

On page 66, there is an error in the code in Exercise 2(f): the line\
college\['Elite'] = pd.cut(college\['Top10perc'], \[0,0.5,1], labels=\['No', 'Yes'])\
should be replaced with\
college\[“Elite”] = pd.cut(college\[“Top10perc”]/100, \[0, 0.5, 1], labels = \[“No”, “Yes”]).\
&#xNAN;_&#x54;hanks to Dylan Owens._

On page 66, Exercise 8(f): the second argument of \`pd.cut\` should be \`\[0, 50, 100]\`. _Thanks to Pedro Zühlke._

In the footnote on the bottom of page 76, the sentence "Details of how to compute the 95% confidence interval precisely in R will be provided later in this chapter" should mention Python instead of R. _Thanks to Rush Kirubi._

On the bottom of page 81, the sentence “Any statistical software package can be used to compute these coefficient estimates, and later in this chapter we will show how this can be done in R.” should mention Python instead of R. _Thanks to Jasmin Bogatinovski and Omar Mallick._

On pages 87, 236, 601, “Mallow’s Cp” should be written as “Mallows’ Cp”. _Thanks to James MacKinnon._

On the top of page 94: The sentence “It is estimated that those in the South will have $18.69 less debt than those in the East, and that those in the West will have $12.50 less debt than those in the East” should instead say “It is estimated that those in the West will have $18.69 less debt than those in the East, and that those in the South will have $12.50 less debt than those in the East. _Thanks to Yongjun Zhu and Felipe Provezano Coutinho._

On page 117, "python" should be "Python", and “rmvar” should be “rm”. _Thanks to Pedro Zühlke._

On page 120, “Prediction intervals are computing” should say “Prediction intervals are computed.” _Thanks to Pedro Zühlke._

On page 121, third line after the first code cell: "exisiting" should be "existing". _Thanks to Pedro Zühlke._

On page 121, 2nd line below 2nd code cell: \`\*kwargs\` should be \`\*\*kwargs\`. _Thanks to Pedro Zühlke._

On page 126, penultimate line before the first code cell: "why their are" should be "why there are". _Thanks to Pedro Zühlke and Guilherme Roma.._

On page 131, exercise 11d: "Show algebraically, and confirm numerically in R" should read "Show algebraically, and confirm numerically in Python". _Thanks to Julien Gomes._

On page 131, exercise 11f should mention Python, not R. _Thanks to anonymous._

On page 141, second paragraph, 6th line: "using statistical software such as R” should say “using statistical software”. _Thanks to Pedro Zühlke._

On page 158, fourth paragraph, 2nd and 3rd lines: Double "instead" in "Instead of assuming..., we instead make ...". _Thanks to Pedro Zühlke._

On the bottom of page 184, the last sentence is missing two words. It should read: “In this case Purchase has only Yes and No values and **the method** returns how many values of each there are.” _Thanks to Johannes Ruf._

On page 187, the printed text under “In\[60]:” should not be in green. _The authors._

On page 188, there are a series of typos, all due to an error in code block 61. In code block 61, the line\
logit\_labels = np.where(logit\_pred\[:,1] > 5, 'Yes', 'No')\
should instead say\
logit\_labels = np.where(logit\_pred\[:,1] > 0.5, 'Yes', 'No')\
With this typo corrected, a correction is also needed before code block 62: the first column of the contingency table should contain “931, 2” instead of “933, 0”.\
Finally, in the text that follows, the sentence “If we use 0.5 as the predicted probability cut-off for the classifier, then we have a problem: none of the test observations are predicted to purchase insurance.” should be corrected as follows: “If we use 0.5 as the predicted probability cut-off for the classifier, then we have a problem: only two of the test observations are predicted to purchase insurance.”\
&#xNAN;_&#x54;hanks to Lauren Chen._

On page 196, exercise 12d, the last two estimates should have the subscript “apple” instead of “orange”. _Thanks to Sundong Kim._

On page 212, line 7: “R” should be replaced with “Python”. _Thanks to_ _Salena Torres Ashton._

On page 214, Figure 5.10: it would be better for the histogram axis to be labeled $\hat\alpha$ rather than $\alpha$. _Thanks to_ _Salena Torres Ashton._

On page 214, 7th line from the bottom: in the line “In particular the bootstrap estimate SE(\hat\alpha) from (5.8) is 0.087,” there should be a subscript “B” on “SE”. _Thanks to Pedro Zühlke._

On page 216, line preceding the last code cell: "training and test set" should be "training and test sets". _Thanks to Pedro Zühlke._

On page 218, 4th line below the first output (Out\[9]): for consistency with the remainder of the chapter, the 'K' in "K results in K-fold ..." should be in lowercase. A similar comment applies on page 219 for the three occurrences of K in the paragraph above the second cell, and the single occurrence in each of the two paragraphs below that same code cell; moreover, this last occurrence should be italicized. _Thanks to Pedro Zühlke._

On page 219, penultimate line above the last code cell: "funtion to implement" should be "function to implement". _Thanks to Pedro Zühlke and Titus Teodorescu._

On page 223, in the penultimate paragraph, the line “Now although the formula for the standard errors do not…” should say “Now although the formulas for the standard errors do not….” _Thanks to Pedro Zühlke._

On page 225, there’s an error in the code for performing the bootstrap. The line\
store\[i] = np.sum(rng.choice(100, replace=True) == 4) > 0\
should be replaced with\
store\[i] = np.sum(rng.choice(100, size=100, replace=True) == 4) > 0\
&#xNAN;_&#x54;hanks to Alistair Bertrand Sands Keiller._

On page 227, Exercise 8c): data.frame() should be replaced by pd.DataFrame(). _Thanks to Adrian Hayler._

On page 231, Algorithm 6.1, Step 3: delete the extra word “using”. _Thanks to Mario Pepe._

On page 235, 2nd paragraph after Algorithm 6.3, 1st line: "requires that the number ... is larger" should be "requires that the number ... be larger". _Thanks to Pedro Zühlke._

On page 263, 5 lines from the bottom: “a simple least squares regression line” should say “a least squares regression”. _Thanks to Pedro Zühlke._

On page 274, middle of the page: “….corresponding to the value 0.114 for the….” should say “….corresponding to the value 0.0114 for the”. _Thanks to Pedro Zühlke._

On page 282, bottom of the page: “is little noticable difference” should say “is little noticeable difference”. _Thanks to Pedro Zühlke._

On page 316, the output of command "In\[18]" should have "bs(age)" instead of "bs(age, knots)". _Thanks to Marcin Łukasik._

On page 334, line preceding (8.3): "minimize the equation" should be "minimize the expression". _Thanks to Pedro Zühlke._

Figure 8.3, bottom left: To be consistent with the text, the labels at the nodes should have the form "X < t" instead of "X <= t". _Thanks to Pedro Zühlke._

On page 355, the output of cell \[6] should be 0.79 instead of 0.7275. _Thanks to Karlo Delic._

On page 358, there is an error in the confusion table. Instead of \[108 61, 10 21] it should say \[94 32, 24 50]. _Thanks to Lauren Chen._

On page 358, “pruned true” should say “pruned tree”. _Thanks to Pedro Zühlke._

On page 362, middle of the page: “leads to a almost the same test MSE as when” should say “leads to almost the same test MSE as when”. _Thanks to Pedro Zühlke._

On page 363, Exercise 3 should mention Python, not R. _Thanks to Marcin Łukasik._

On page 365, Exercise 9f and Excercise 9h are redundant. _Thanks to Pedro Zühlke._

On page 387, in the first paragraph of Section 9.6.1, “When the cost argument is small” should say “When the C argument is small”. _Thanks to Ameer Dharamshi._

On the bottom of page 414, the mention of _glmnet_ should be replaced with a mention of _sklearn_. _Thanks to Pedro Zühlke._

On page 420, second paragraph: the word “accompanying” is misspelled. _Thanks to Pedro Zühlke._

On page 438, we define standard\_lasso in cell \[14] and never use it. We have changed the lab slightly, and now cell \[15] and \[16] are slightly modified. Pick up the modified lab from the GitHub site linked [here](https://github.com/intro-stat-learning/ISLP_labs/tree/stable). _Thanks to Martin Storath_.

On page 460, before code block 65: “convert it to our a more familiar” should say “convert it to a more familiar”. _Thanks to Pedro Zühlke._

On page 486, the x-axis of Figure 11.7 is missing a vertical line in the denominator (i.e. a single vertical line should be replaced with a double vertical line in the norm symbol).

On the bottom of page 511: “we can use (12.11) to see that the PVE defined in (12.10) equals . . . ” should be replaced with “we can use (12.11) to see that the PVE defined in (12.10), summed over the first $M$ principal components, equals . . .”. _Thanks to Zhuyun Yin._

On page 508, 4th line after the table: the reference to Table 12.2.1 should mention Table 12.1. _Thanks to Pedro Zühlke._

On page 512, Figure 12.3: it would be better for the x-axis to not display increments of 0.5, since the figure displays principal component indices, which are discrete. _Thanks to Salena Torres Ashton._

On page 535, top of Section 12.5: “scanning the first few lines . . . tell us” should be “scanning the first few lines . . . tells us”. _Thanks to Pedro Zühlke._

On page 549, Figure 12.18 caption: “100,%” should be “100%”. _Thanks to Pedro Zühlke._

On page 551, 1st line after code cell \[56]: extra word "line" in "draws a horizontal line line". _Thanks to Pedro Zühlke._

On page 561, the sentence “Typically, the R function that is used to compute a test statistic will make…” should mention Python, not R. _Thanks to Yongjun Zhu._
