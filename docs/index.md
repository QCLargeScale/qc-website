# 🚀 Quantum Computing for Solving Large-Scale Linear Systems

**Hybrid: Classical and Quantum solutions for scientific computing**


!!! info "Project Information"
    <div style="text-align: center;">
    <strong>Dr. Ezhilmathi Krishnasamy</strong><br>
    Author and Principal Investigator<br>
    Science and Technology Centre Novo Mesto
    
    Funded by the Slovenian Research & Innovation Agency (ARIS)  
    under the Early-Stage Researchers funding scheme  
    [(Grant No. ARIS-RZK-2025/54)](https://www.aris-rs.si/sl/inovac/rezultati/26/inc/Seznam-RZK-febr26.pdf)
    </div>	


# Overall Concept

Prior to the advent of quantum computing, mathematical modeling using classical computers was employed to address problems arising from science and engineering. This process, known as **scientific computing**, involves solving complex computational problems using multiple processes.

Over the years, there have been tremendous advancements in technology, particularly with the development of electronics, leading to modern processors and accelerators. This evolution has facilitated the application of advanced approaches for solving partial differential equations (PDEs), which are typically addressed using numerical methods. The resulting systems of equations can then be solved efficiently using supercomputing resources.

At present, classical processors are limited by three fundamental barriers: the **memory wall**, the **Instruction-Level Parallelism (ILP) wall**, and the **power wall** [2](https://www.sciencedirect.com/book/9780123838728/computer-architecture).

Although these challenges may be mitigated in the coming years due to ongoing advancements in electronics, there is no guarantee that they will be completely resolved. Despite the exponential growth in computing power, there remains a need to explore alternative approaches.

Historically, innovation has always been driven by exploring alternatives. From early vacuum-tube-based computers to modern electronic chips and accelerators, progress has relied on continuous evolution. In this context, **quantum computing** emerges as a promising candidate for advancing computational efficiency.

Quantum computers offer several potential advantages over classical systems, including improved energy efficiency [5](https://journals.aps.org/prxquantum/abstract/10.1103/PRXQuantum.3.020101) and significantly faster computation for specific problems [3](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.127.180501).

For example, factoring a large number with \( n \) bits requires exponential time on classical computers (approximately \( \exp(n^{1/3}) \)), whereas a quantum computer using **Shor’s algorithm** can solve it in polynomial time (approximately \( O(n^2 \log n) \)) [6](https://doi.org/10.1137/S0036144598347011).

Considering future growth in computational power, reach, and energy efficiency, quantum computing presents a significant opportunity for solving computationally intensive problems.

One of the most demanding domains is solving systems of equations derived from differential equations. Linear systems often rely on **Basic Linear Algebra Subprograms (BLAS)**, which are fundamental to machine learning (ML) and artificial intelligence (AI). Advancing solutions for large-scale linear systems on quantum computers could lead to breakthroughs in science and engineering.

Examples of challenging applications include:

- Fluid dynamics simulations such as Large Eddy Simulation (LES) [7](https://www.sciencedirect.com/science/article/pii/S154074892300270X) and Direct Numerical Simulation (DNS) [8](https://aip.scitation.org/doi/10.1063/5.0129929)
- Plasma physics problems such as tokamak modeling for energy production [9](https://iopscience.iop.org/article/10.1088/1361-6587/ac4b0a)
- Large-scale data analysis, including data from the James Webb Space Telescope [10](https://www.icds.psu.edu/machine-learning-takes-starring-role-in-exploring-the-universe/)

Quantum computing has the potential to significantly improve the efficiency of solving such problems.

---

# Core Ideas and Assumptions

The following key ideas and assumptions guide the development of software frameworks for solving large linear systems:

1. Develop a software framework specifically designed for efficiently solving large linear systems on a simulator.  
2. Extend this methodology to incorporate hybrid computing techniques.  
3. Ensure full utilization of quantum computation to enhance problem-solving capabilities.  

These approaches will be connected to practical applications in:

- Machine learning (ML)  
- Artificial intelligence (AI)  
- Engineering and computational physics problems involving PDEs  

---

# Transdisciplinary Approach

Quantum computing is inherently interdisciplinary. To achieve productive outcomes, collaboration across multiple domains is essential:

- Software platforms such as [Qiskit](https://qiskit.org), [PennyLane](https://pennylane.ai), and [Ocean SDK](https://docs.ocean.dwavesys.com)
- Quantum architecture research teams  
- Experts in classical computer architecture  
- Domain specialists in:
   - Machine learning  
   - Artificial intelligence  
   - Plasma physics  

Engaging with these diverse groups will foster a rich and productive research environment. Continuous knowledge exchange and collaboration are crucial for improving the effectiveness and impact of the project.

---

# Linked Research and Innovation Activities

At the national level, Slovenia is actively investing in quantum computing research. Notably, the **Center for Light, Matter, and Quanta** at the Josef Stefan Institute [11](https://plus.ijs.si/) aims to position Slovenia at the forefront of quantum technologies.

At the European Union level, there has been substantial investment in quantum computing research and innovation [12](https://digital-strategy.ec.europa.eu/en/library/quantum-europe-strategy). The EU is also planning the deployment of quantum computers across member states [13](https://eurohpc-ju.europa.eu/eurohpc-quantum-computers_en).

These initiatives will:

- Strengthen quantum infrastructure  
- Promote collaboration  
- Accelerate technological development  

Through this project, we aim to collaborate with national and EU-level partners to enhance infrastructure access and facilitate knowledge sharing.

---

# Partners

- Rudolfovo Science and Technology, Novo Mesto  
- University of Ljubljana  
- University of Luxembourg  
- Simula Research Laboratory  
- University of Oslo

# References

[2] Hennessy, J. L., & Patterson, D. A. *Computer Architecture: A Quantitative Approach*.  
https://www.sciencedirect.com/book/9780123838728/computer-architecture  

[3] Wu, Y., et al. "Strong quantum computational advantage using a superconducting quantum processor."  
https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.127.180501  

[5] Auffèves, A. "Quantum technologies need a quantum energy initiative."  
https://journals.aps.org/prxquantum/abstract/10.1103/PRXQuantum.3.020101  

[6] Shor, P. W. "Polynomial-time algorithms for prime factorization and discrete logarithms."  
https://doi.org/10.1137/S0036144598347011  

[7] Mira, D., et al. "HPC-enabling technologies for high-fidelity combustion simulations."  
https://www.sciencedirect.com/science/article/pii/S154074892300270X  

[8] Dang, G., et al. "Direct numerical simulation of compressible turbulence."  
https://aip.scitation.org/doi/10.1063/5.0129929  

[9] Litaudon, X., et al. "EUROfusion theory and advanced simulation coordination."  
https://iopscience.iop.org/article/10.1088/1361-6587/ac4b0a  

[10] Machine learning and JWST data  
https://www.icds.psu.edu/machine-learning-takes-starring-role-in-exploring-the-universe/  

[11] Center for Light, Matter, and Quanta  
https://plus.ijs.si/  

[12] EU Quantum Strategy  
https://digital-strategy.ec.europa.eu/en/library/quantum-europe-strategy  

[13] EuroHPC Quantum Computers  
https://eurohpc-ju.europa.eu/eurohpc-quantum-computers_en  
