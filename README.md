
-------

<div align="center">

<h1> Michael Staneker </h1>

</div>

<p align="center">
	<a href="https://github.com/MichaelSt98">
		<img src="https://img.shields.io/badge/-GitHub-000?style=for-the-badge&logo=Github&logoColor=white"/>
	</a>
	<a href="https://www.linkedin.com/in/michael-staneker">
		<img src="https://img.shields.io/badge/Linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
	</a>
</p>

<div align="center">
<br>
Currently finishing my master's degree in physics at the <a href="https://uni-tuebingen.de/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/physik/institute/astronomie-und-astrophysik/computational-physics/willkommen/">University of Tübingen</a>.
</br>
</div>

-------

<div align="center">
<h3> Some ... </h3>
</div>

<div align="center">
<h3> languages </h3>
</div>

<div align="center">
<p>
<img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white" alt="C" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" alt="C" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/python%20-%2314354C.svg?&style=for-the-badge&logo=python&logoColor=white" alt="python" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/shell_script%20-%23121011.svg?&style=for-the-badge&logo=gnu-bash&logoColor=white" alt="bash" />&nbsp;&nbsp;
</p>
</div>

<div align="center">
<h3> databases </h3>
</div>

<div align="center">
<p>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="mysql" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" alt="mysql" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="mysql" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/Apache_Hadoop-66CCFF?style=for-the-badge&logo=apachehadoop&logoColor=white" alt="mysql" />&nbsp;&nbsp;
</p>
</div>

<div align="center">
<h3> operating systems </h3>
</div>

<div align="center">
<p>
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="linux" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/MacOS-000000?style=for-the-badge&logo=macos&logoColor=white" alt="linux" />&nbsp;&nbsp;
</p>
</div>

<div align="center">
<h3> and other stuff </h3>
</div>

<div align="center">
<p>
<img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="git" />&nbsp;&nbsp;
<img src="https://img.shields.io/badge/latex-008080?style=for-the-badge&logo=latex&logoColor=white" alt="git" />&nbsp;&nbsp;
</p>
</div>

<div align="center">
<h3> I already worked with and like. </h3>
</div>


------------


<h3> Projects </h3>


<h4> MilupHPC </h4>


<table>
  <tr>
    <td valign="top" align="left" width="500">
    <ul>
      <li>A HPC N-Body and Smooth(ed) Particle Hydrodyamics (SPH) code via <br>CUDA-aware MPI</br> targeting distributed memory systems</li>
      <li>For 1, 2 and 3 dimensional simulation</li>
      <li>Dynamic load balancing using space-filling curves</li>
      <li>Current test cases:</li>
      <ul>
      <li>Plummer model</li>
      <li>Taylor–von Neumann–Sedov blast wave</li>
      <li>Isothermal collapse of a molecular cloud (Boss & Bodenheimer)</li>
	 </ul>
    </ul>
    <a href="https://github.com/MichaelSt98/MilupHPC">
        <img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=MichaelSt98&repo=MilupHPC" />
      </a>
    </td>
    <td align="center" width="500">
    <img src="gifs/4proc_plummer_dynamic.gif" alt="sample plummer model"  width="400" />
    </td>
  </tr>
</table>


<details>
  <summary>More information ...</summary>
  
This repository aims to implement a **Multi-GPU SPH/NBody algorithm using CUDA aware MPI** by combining ideas from:

* **Single-GPU version inspired/adopted from:**
	* [Miluphcuda](https://github.com/christophmschaefer/miluphcuda) 
	* [An Efficient CUDA Implementation of the Tree-Based Barnes Hut n-Body Algorithm](https://iss.oden.utexas.edu/Publications/Papers/burtscher11.pdf)
	* [Implementation: MichaelSt98/NNS](https://github.com/MichaelSt98/NNS/tree/main/3D/CUDA/CUDA_NBody) CUDA\_NBody
* **Multi-Node (or rather Multi-CPU) version inspired/adopted from:**
	* M. Griebel, S. Knapek, and G. Zumbusch. Numerical Simulation in Molecular Dynamics: Numerics, Algorithms, Parallelization, Applications. 1st. Springer Pub- lishing Company, Incorporated, 2010. isbn: 3642087760
	* [Implementation: MichaelSt98/NNS (branch: MolecularDynamics)](https://github.com/MichaelSt98/NNS/tree/MolecularDynamics/MolecularDynamics/BarnesHutParallel)


* some more samples: each color represents a process, thus a GPU
* **Kepler disk**
	* Kepler disk: four GPUs (hilbert curve)

<img src="gifs/kepler_hilbert_4proc.gif" alt="Plummer"  width="400" />

* **Plummer model**
	* four GPUs with dynamic load balancing every 10th step (top: lebesgue, bottom: hilbert)

<img src="gifs/4proc_plummer_dynamic.gif" alt="Plummer"  width="400" />

* **Taylor–von Neumann–Sedov blast wave**
	* Sedov explosion: one and two GPUs

<img src="gifs/sedov_sample_movie.gif" alt="Sedov"  width="400" />

* **Boss-Bodenheimer: isothermal collapse**
	* one and two GPUs 

<img src="gifs/bb_sample_movie.gif" alt="Boss Bodenheimer"  width="400" />

</details>

------------



