# RPTree
This project explores Rare Pattern Assocation Mining by taking implementing the FP-Tree data structure.
The goal is to accumulate all rare patterns by definition ("RP-Tree: Rare Pattern Mining", A. Cuzzocrea and U. Dayal (Eds.): Data Warehousing and Knowledge Discovery 2011, LNCS 6862, pp. 277–288, 2011.) within a given transactional data set in a more efficient 
manner. In these project files, we have modified existing FP (frequent pattern) code within the SPMF package (which can be found available here :http://www.philippe-fournier-viger.com/spmf/index.php?link=download.php). The files available in the repository are subsets of the SPMF v2.36 package

# Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and
testing purposes.

# Prerequisites
To run the project it is suggested to use a IDE such as Eclipse. 

# Installing
Once Eclipse has been installed go through the following steps to execute the project:
* Open Eclipse. Select "File -> New -> Java Project"
* Type the name of the project and select "Finish"
* Once your project is created, "Select your project name -> new -> package"
* Name your package "rpTree" (NOTE: if you use a different package name, you will manually need to adjust all imports/packages)
* Download the files from Project Files and move the files to the package location
  * To do this: "Right click package -> properties -> open source in system explorer (right side of the location textbox)
  * Open the "rpTree" folder -> bring files into this location
* The project is now able to be compiled.

# Running the Tests
To run the test, open up the "MainTestAllAssociationRules_RPGrowth.java" file. The text file name has already been set ("contextRP.txt"), and for the purpose of the default test the minsup (which serves as the maximum threshold of our rare rules) and the minraresup (which serves as the minimum threshold of our rare rules) have been set at 0.6 and 0.1 accordingly.

# Example Test Run
After getting everything set up properly; running the main test with the supplied test file and support constraints will produce the following output:
NOTE: in between the rare itemset list and the association rules is a stats section.
 * ------- RARE ITEMSETS -------
 * L0
 * L1
 * pattern 0: 4 support : 1
 * L2
 * pattern 1: 1 4 support : 1
 * pattern 2: 2 4 support : 1
 * L3
 * pattern 3: 1 2 4 support 1
 * -------------------------------
 * ------- ASSOCIATION RULES -------
 * rule 0: 4 ==> 1 support : 0.2 (1/5) confidence : 1.0
 * rule 1: 4 ==> 2 support : 0.2 (1/5) confidence : 1.0
 * rule 2: 2 4 ==> 1 support : 0.2 (1/5) confidence : 1.0
 * rule 3: 1 4 ==> 2 support : 0.2 (1/5) confidence : 1.0
 * rule 4: 4 ==> 1 2 support : 0.2 (1/5) confidence : 1.0
 
NOW an example increasing the minsup to .8

 * ------- RARE ITEMSETS -------
 * L0
 * L1
 * pattern 0: 4 support : 1
 * pattern 1: 5 support : 3
 * L2
 * pattern 2: 1 4 support : 1
 * pattern 3: 2 4 support : 1
 * pattern 4: 1 5 support : 2
 * pattern 5: 3 5 support : 3
 * pattern 6: 2 5 support : 3
 * L3
 * pattern 7: 1 2 4 support : 1
 * pattern 8: 1 3 5 support : 2
 * pattern 9: 2 3 5 support : 3
 * pattern 10: 1 2 5 support : 2
 * L4
 * pattern 11: 1 2 3 5 support : 2
 * -------------------------------
 * ------- ASSOCIATION RULES -------
 * rule 0:  4 ==> 1 support :  0.2 (1/5) confidence :  1.0
 * rule 1:  5 ==> 1 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 2:  4 ==> 2 support :  0.2 (1/5) confidence :  1.0
 * rule 3:  5 ==> 2 support :  0.6 (3/5) confidence :  1.0
 * rule 4:  5 ==> 3 support :  0.6 (3/5) confidence :  1.0
 * rule 5:  2 4 ==> 1 support :  0.2 (1/5) confidence :  1.0
 * rule 6:  1 4 ==> 2 support :  0.2 (1/5) confidence :  1.0
 * rule 7:  4 ==> 1 2 support :  0.2 (1/5) confidence :  1.0
 * rule 8:  2 5 ==> 1 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 9:  1 5 ==> 2 support :  0.4 (2/5) confidence :  1.0
 * rule 10:  5 ==> 1 2 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 11:  3 5 ==> 1 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 12:  1 5 ==> 3 support :  0.4 (2/5) confidence :  1.0
 * rule 13:  5 ==> 1 3 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 14:  3 5 ==> 2 support :  0.6 (3/5) confidence :  1.0
 * rule 15:  2 5 ==> 3 support :  0.6 (3/5) confidence :  1.0
 * rule 16:  5 ==> 2 3 support :  0.6 (3/5) confidence :  1.0
 * rule 17:  2 3 5 ==> 1 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 18:  1 3 5 ==> 2 support :  0.4 (2/5) confidence :  1.0
 * rule 19:  1 2 5 ==> 3 support :  0.4 (2/5) confidence :  1.0
 * rule 20:  3 5 ==> 1 2 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 21:  2 5 ==> 1 3 support :  0.4 (2/5) confidence :  0.6666666666666666
 * rule 22:  1 5 ==> 2 3 support :  0.4 (2/5) confidence :  1.0
 * rule 23:  5 ==> 1 2 3 support :  0.4 (2/5) confidence :  0.6666666666666666
 
 
 
# Explaination of the Data
 The "RARE ITEMSETS" section displays the particular rare rules that have been derived from the original data set. This is representating the number of time said item or pair of items occured together. Increasing and decreaing the minsup or minraresup variables adjust the range of support of what is considered "rare" (as you can see in the difference between the first example and the second).
  The "ASSOCIATION RULES" section displays the complete association breakdown between the set and the implication (e.g. in example 2: "rule 18: 1 3 5 ==> 2 support : 0.4 (2/5) confidence : 1.0"). This represents the implication between X ==> Y, the support for said implication (in percentage and rationale representation), and the confidence of this occurance (expressed in percentage)

 
# Contributing
If pulled and changes are made please branch initially. Once changes are stable please merge and include name, date of change, and your fix to the code in the comments of the corresponding source file and in the merge comments.

# Authors
 * Ryan Benton - Initial Work - rgbenton
 * Blake Johns - Initial Work - Mr-Shisha

# License
* These files are copyright (c) 2008-2012 Philippe Fournier-Viger
* 
* These file are part of the SPMF DATA MINING SOFTWARE
* (http://www.philippe-fournier-viger.com/spmf).
* 
* SPMF is free software: you can redistribute it and/or modify it under the
* terms of the GNU General Public License as published by the Free Software
* Foundation, either version 3 of the License, or (at your option) any later
* version.
* SPMF is distributed in the hope that it will be useful, but WITHOUT ANY
* WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR
* A PARTICULAR PURPOSE. See the GNU General Public License for more details.
* You should have received a copy of the GNU General Public License along with
* SPMF. If not, see <http://www.gnu.org/licenses/>.

# Acknowledgements
 * This is a modification of existing FP (frequent pattern) code and an implementation of the FPGROWTH algorithm (Han et al., 2004). Han, J., Pei, J., & Yin, Y. (2000, May). Mining frequent patterns without candidate generation. In ACM SIGMOD Record (Vol. 29, No. 2,    pp. 1-12). ACM.
 The source code can be found here: http://www.philippe-fournier-viger.com/spmf/index.php?link=download.php The files included are a subset of the SPMF v2.36 package.
 * A. Cuzzocrea and U. Dayal (Eds.): Data Warehousing and Knowledge Discovery 2011, LNCS 6862, pp. 277–288, 2011.
