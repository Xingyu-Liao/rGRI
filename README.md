Latest Version
==============
Please see the latest version of rGRI:https://github.com/Xingyu-Liao/rGRI


License
=======

Copyright (C) 2020 Xingyu Liao(liaoxingyu@csu.edu.cn)

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 3
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, see <http://www.gnu.org/licenses/>.

Xingyu Liao(liaoxingyu@csu.edu.cn)
School of Computer Science and Engineering
Central South University
ChangSha
CHINA, 410083


Installation and operation of rGRI 
==================================

### Dependencies

When running rGRI from GitHub source the following tools are required:

* [jdk 1.8.0 or above]
* [GNU C++ 4.6.3 or above] 
* [perl 5.6.0 or above] 
* [python 2.7.14 or above]
 
### Install rGRI

rGRI is written Java and therefore will require a machine with jdk pre-installed.

Create a main directory (eg:rGRI). Copy all source code to this directory.

Running of the following command to compile the rGRI: 

javac rGRI.java 

### Run rGRI.
	
    Running command:  
	java -Xmx256G rGRI -r [ /home/reference.fa | /home/assemblies.fa ] -k [49] -m [5000] -f [/home/reference.fa] -Q [yes/no] -M [yes/no] -t [8] -o [/home/finalResults/] [options] 
	
	[options]
	
	     -Xmx256G <This parameter is only used when processing large datasets (For example: the genome size exceeds 5Gb)>
	     -r <The reference file or the assemblies file>
	     -k <The k-mer size used during the detection(Default value: 49)>
	     -t <The number of threads(Default value: 8)>
        -M <This parameter controls whether the alignment rate of detection results is counted(Setting this parameter to 'yes' indicates statistics)>
        -Q <This parameter controls whether the effective size of detection results is counted(Setting this parameter to 'yes' indicates statistics)>
	     -f <The reference file used for results evaluation>
             -o <The path used to save the final detection results>		 
	
	[extremely]
	
	If the system prompts "operation not permitted" ,we need to run the following commands to modify the permissions of rGRI-master folder at this time.
    
	cd ..
	chmod -R 777 rGRI-master
	cd rGRI-master
	java rGRI
	
### Output.
    
	(1)The final detection results will be stored in the path specified by '-o'.
	
    If the value of '-o' is set to '/home/output', the final detection results will be stored in '/home/output'.
	Otherwise, the detection results will be stored in the default path (.../rGRI-master/FinalRepeatLib/).

