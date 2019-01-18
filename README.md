# RPTree
This project explores Rare Pattern Assocation Mining by taking advantage of the FP-Tree data structure.
The goal is to accumulate all rare patterns (by our definition) within a given data set in a more efficient 
manner. 

# Getting Started
These instruction swill get you a copy of the project up and running on your local machine for development and
testing purposes. See deployment for notes on how to deploy the project on a live system.

# Prerequisites
To run the project it is suggested to use a IDE such as Eclipse. 

# Installing
Once Eclipse has been installed go through the following steps to execute the project:
* Open Eclipse. Select "File -> New -> Java Project"
* Type the name of the project and select "Finish"
* Once your project is created, "Select your project name -> new -> package"
* Name your package
* Download the files from Project Files and move the files to the package location
  * To do this: "Right click package -> properties -> open source in system explorer (right side of the location textbox)
  * Open the "src" folder -> bring files into this location
* Adjust the package name / import calls to fit your personal created package name.

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
 * pattern 2: 2 4 support : 4
 * L3
 * pattern 3: 1 2 4 support 1
 * -------------------------------
 * ------- ASSOCIATION RULES -------
 * rule 0: 4 ==> 1 support : 0.2 (1/5) confidence : 1.0
 * rule 1: 4 ==> 2 support : 0.2 (1/5) confidence : 1.0
 * rule 2: 2 4 ==> 1 support : 0.2 (1/5) confidence : 1.0
 * rule 3: 1 4 ==> 2 support : 0.2 (1/5) confidence : 1.0
 * rule 4: 4 ==> 1 2 support : 0.2 (1/5) confidence : 1.0
 
# Contributing

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
 This is an implementation of the FPGROWTH algorithm (Han et al., 2004).
 Han, J., Pei, J., & Yin, Y. (2000, May). Mining frequent patterns without candidate generation. In ACM SIGMOD Record (Vol. 29, No. 2,    pp. 1-12). ACM.
 The source code can be found here: http://www.philippe-fournier-viger.com/spmf/index.php?link=download.php
