# Matrice-Gauss-and-Cramer-Model
Interactive Cramer and Gauss app: 10 manufacturing cases, step-by-step calculations and checks online.    Make my English exactly 100 characters
from pathlib import Path
import pypandoc

readme = """# Cramer and Gauss Methods – Manufacturing SPL Laboratory

An interactive learning tool for solving linear systems using Cramer's Rule and Gaussian Elimination through 10 manufacturing case studies.

## Overview

This project is an HTML-based educational simulator for **Mathematical Engineering 1 (Week 10)**. It helps students understand, calculate, and compare two methods for solving systems of linear equations (SPL).

## Learning Features

- Step-by-step solution using **Cramer's Rule**.
- Step-by-step **Gaussian Elimination** using elementary row operations.
- Determinant calculations for 2 × 2 and 3 × 3 coefficient matrices.
- Augmented matrix formation and pivot selection.
- Back-substitution to obtain variable values.
- Automatic comparison of both methods.
- Substitution-based verification of calculated solutions.
- Editable coefficients and constants for experimentation.
- Detection of unique, inconsistent, and infinitely many-solution systems.

## Manufacturing Case Studies

The simulator includes 10 illustrative cases:

1. Two-component production planning.
2. Work-hour allocation for two assembly stations.
3. Two-raw-material mixing formulation.
4. Operating-hour requirements for two machine types.
5. Three-product production lot planning.
6. Three-material mixing balance.
7. Operator allocation across three activities.
8. Three-material requirement planning.
9. Calibration of three machining parameters.
10. Reconciliation of three production cost groups.

## How to Use

1. Download `sourcecode_metode_cramer_gauss_10_studi_kasus_manufaktur.html`.
2. Open the HTML file in a modern web browser (Google Chrome, Microsoft Edge, or Firefox).
3. Select one of the 10 manufacturing case studies.
4. Review the problem description and its mathematical model.
5. Modify matrix coefficients or right-hand-side constants if needed.
6. Select **Hitung kedua metode** to calculate the solution.
7. Review the Cramer and Gaussian Elimination steps.
8. Compare the results and inspect the substitution verification.

## Mathematical Model

The simulator uses the matrix representation:

\\[
AX = B
\\]

where:

- \\(A\\) is the square coefficient matrix of order \\(n \\times n\\).
- \\(X\\) is the variable vector of order \\(n \\times 1\\).
- \\(B\\) is the constant vector of order \\(n \\times 1\\).

For Cramer's Rule:

\\[
x_i = \\frac{\\det(A_i)}{\\det(A)}, \\qquad \\det(A) \\ne 0
\\]

Gaussian Elimination transforms the augmented matrix \\([A \\mid B]\\) using elementary row operations, followed by back-substitution.

## Requirements

- A modern web browser.
- No installation, server, or external library is required.
- The simulator runs locally in the browser.

## Important Notes

The case studies are simplified educational models. Their numerical values are intended for learning linear algebra procedures and should not be interpreted as validated industrial operating data.

For real manufacturing applications, validate the model assumptions, units, data, and constraints. Production quantities may also require non-negativity, integer, capacity, and demand constraints.

## License

No license has been specified. Add a license file before redistributing or reusing this project under formal open-source terms.
"""
out = Path("/mnt/data/README_Cramer_Gauss_Manufacturing.md")
pypandoc.convert_text(readme, "md", format="md", outputfile=str(out), extra_args=["--standalone"])
print(f"Created: {out} ({out.stat().st_size:,} bytes)")
