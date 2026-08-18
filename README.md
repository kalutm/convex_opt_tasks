# Convex Optimization Tasks

This repository contains practical implementations and benchmarks for convex optimization problems formulated and solved using **CVXPY**.

---

> ⚠️ **Viewing Note:**  
> GitHub's native Jupyter notebook renderer often times out or fails to render plots.  
> **Please view the fully rendered notebook directly on NBViewer:**  
> 👉 **[View Rendered Notebook on NBViewer](https://nbviewer.org/github/kalutm/convex_opt_tasks/blob/main/Convex_Opt_Tasks.ipynb)**

---

## Repository Overview

### Task 2: Primal Soft-Margin Support Vector Machine (SVM)
- **Formulation:** Formulated the primal soft-margin SVM as a Convex Quadratic Program (QP).
- **Solver:** Solved using CVXPY and compared directly against `scikit-learn`'s `LinearSVC`.
- **Key Deliverables:**
  - Solver convergence verification.
  - Hyperparameter analysis across multiple error penalty values ($C = 0.01, 1.0, 100.0$).
  - Decision boundary plots comparing CVXPY and scikit-learn implementations.

### Task 3: Markowitz Mean-Variance Portfolio Optimization
- **Formulation:** Implemented the classic Markowitz portfolio selection model using an expected returns vector ($\mu$) and a positive semi-definite covariance matrix ($\Sigma$).
- **Constraints:**
  - Exact budget allocation: $\sum w_i = 1$
  - Long-only constraints (no short-selling): $w_i \ge 0$
- **Key Deliverables:**
  - Solver execution status and optimal allocation weights output.
  - Risk-return trade-off analysis (Efficient Frontier) across varying risk-aversion parameters ($\gamma$).

---

## Setup & Local Execution

To run the notebook locally using `uv`:

```bash
# Clone repository
git clone [https://github.com/kalutm/convex_opt_tasks.git](https://github.com/kalutm/convex_opt_tasks.git)
cd convex_opt_tasks

# Initialize virtual environment and activate
uv venv
source .venv/bin/activate

# Install dependencies
uv pip install jupyter cvxpy numpy matplotlib scikit-learn

# Launch Jupyter
jupyter notebook