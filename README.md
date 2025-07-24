# Design and Development of Karnaugh Map Simulator to Simplify Boolean Expression

## Metadata
- **Authors**: 
  - Mundhe Anil Krushna (`mundheanil84@gmail.com`)
  - Banale Shashank Santosh (`banaleshashank0804@gmail.com`)
  - Manjusha A. Kanawade (`makanawade_elec@jspmrscoe.edu.in`)
- **Affiliation**: Department of Electrical Engineering, JSPM’S Rajarshi Shahu College of Engineering, Pune, India
- **Keywords**: Boolean Expression, Karnaugh Map, Digital Logic Circuits, Virtual Simulator

## Abstract
This paper presents the design and development of a web-based simulator for simplifying Boolean expressions using Karnaugh Maps (K-maps). The simulator, built with HTML, CSS, and JavaScript, provides an interactive tool for users to input Boolean expressions, visualize K-maps, and obtain simplified expressions. The tool aims to reduce the complexity of digital logic circuits by automating the K-map simplification process, minimizing human error, and improving efficiency.

---

## 1. Introduction
Karnaugh Maps (K-maps) are graphical tools used in digital circuit design to simplify Boolean expressions and minimize gate requirements. While K-maps are effective, manual simplification becomes challenging with increasing variables. This paper introduces a simulator that automates the process, leveraging web technologies for accessibility and interactivity.

### Key Steps in K-map Simplification:
1. Construct a truth table for the Boolean function.
2. Create a K-map with rows/columns labeled by input variables.
3. Fill the K-map with output values from the truth table.
4. Group adjacent cells (implicants) to form simplified expressions.

**Example**:  
For the Boolean function \( F(A,B,C) = \sum(0,2,4,5,7) \), the truth table and K-map are generated (see Table 1 and Fig. 1 in the paper).

---

## 2. Development of the Simulator
### Implementation:
- **Frontend**: HTML/CSS for UI, including input fields, buttons, and K-map visualization.
- **Backend**: JavaScript for logic implementation, including:
  - Truth table generation.
  - K-map population and grouping.
  - Application of the Quine-McCluskey algorithm for simplification.

### Key Features:
1. **User Input**: Supports minterms and "don't care" conditions.
2. **Dynamic Updates**: Real-time K-map rendering based on input changes.
3. **Simplification**: Outputs optimized Boolean expressions (e.g., `F = A'B' + AC`).

### Code Snippets:
- `solveKMap()`: Triggers simplification on button click.
- `createKMap()`: Updates the visual K-map grid.
- `simplifyBooleanFunction()`: Applies Boolean algebra laws for optimization.

---

## 3. Results and Validation
The simulator was tested with multiple Boolean functions and compared against manual simplification. Results confirmed:
- **Accuracy**: Matched manual simplification outputs.
- **Efficiency**: Reduced time and effort for complex expressions.
- **Visualization**: Enhanced understanding through interactive K-maps (see Figs. 4–6).

---

## 4. Future Work
1. **Scalability**: Extend to handle >5 variables.
2. **UI Enhancements**: Add drag-and-drop, real-time highlighting.
3. **Algorithm Comparison**: Benchmark against Quine-McCluskey and BDDs.
4. **Don't Care Optimization**: Improve handling of "don't care" conditions.

---

## 5. Conclusion
The simulator provides an accessible, accurate, and efficient tool for simplifying Boolean expressions using K-maps. Its web-based design ensures compatibility across devices, making it suitable for both education and professional use.

---

## References
1. Huang, J. (2014). *Programming implementation of the Quine-McCluskey method*. [arXiv:1410.1059](https://arxiv.org/ftp/arxiv/papers/1410/1410.1059.pdf).
2. Ahmad, A., et al. *Development of Verification Tool for Minimal Boolean Equation*. IEEE ITEE, 8(3).
3. Abdelrahman, E. (2014). *A C++ Karnaugh Map Minimizer*. [CodeProject](http://www.codeproject.com/Articles/649849/A-Cplusplus-Karnaugh-Map-Minimizer).
4. Gindi, S., et al. (2015). *Simplification of Digital Circuits in OOP*. JISRD, 3(2).
5. Brown, F. M. (2011). *On the Suppression of Variables in Boolean Equations*. Elsevier.

---

**Figures**:  
- Fig. 1: K-map structure for \( F(A,B,C) \).  
- Fig. 2: Variable selection interface.  
- Fig. 3: Truth table creation.  
- Fig. 4–6: Simulator screenshots showing K-map and simplified output.
