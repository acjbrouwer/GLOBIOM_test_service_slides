---
title: The GLOBIOM test service
author: Albert Brouwer
date: 2026-04-15
---

# Outline

- Purpose of the GLOBIOM test service
- History
- Function
- Use
- Scalability and features: reproducible clean-slate tests, special provisions for GLOBIOM testing
- Access for GLOBIOM core team members at https://jenkins.iiasa.ac.at

---

# Purpose: automated testing

Automated testing is essential in scientific software because it enforces rigor, protects reproducibility, and prevents silent regressions that can corrupt results or invalidate published findings. It guarantees that complex numerical pipelines remain trustworthy as models evolve.

---

# Purpose: automated testing of GLOBIOM

- Catches regressions and errors early in the development cycle
- Reduces manual testing burden
- Expands test scope beyond what would be practical otherwise
- Produces metrics for improving model code/performance/outcomes
- Integrates with version control for traceable changes
- Guards cross-platform and containerization compatibility
- Increases confidence in model results

---

# Purpose: automated testing of everyday software

Automated testing for everyday software can be simple and light because most features can be checked in small pieces, one at a time, on a regular laptop. Developers can quickly run these tiny checks while they work, catching mistakes early—long before the software becomes big or complex. This doesn’t require a large testing system or special infrastructure; it’s more like proofreading each paragraph as you write, instead of waiting to review the whole book at the end.

# Purpose: automated testing of big GAMS models

Enormous, data‑heavy GAMS models can’t be tested the way everyday software can because their behavior depends on running the *entire* system at once. They pull in huge datasets and interact through tightly linked equations, so changing one part affects everything else. You can’t check them in tiny pieces on a laptop—only full, time‑consuming runs reveal whether results still make sense. These models behave like whole ecosystems: only by simulating the complete environment can you see if a change truly works.

---

# Purpose: automated testing with Jenkins

Hence a heavily customized automated test setup has been deployed that is capable of handling GLOBIOM testing. It is based on Jenkins.

Jenkins remains the go‑to for demanding scientific environments because it offers unmatched customization, deep plugin extensibility, and full control over execution pipelines. It thrives in Internet-isolated cluster‑bound setups where cloud CI cannot reach. Its robustness, scriptability, and ability to orchestrate heterogeneous local resources make it ideal for long‑running  tests requiring on‑prem autonomy.
