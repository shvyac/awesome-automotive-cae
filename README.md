# Awesome Automotive CAE [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of open-source tools, datasets, and references for **automotive CAE** — crash safety, structural FEA, NVH, CFD / aerodynamics, durability, optimization, and AI surrogates. Prefer durable official / project URLs.
>
> 自動車 CAE（衝突安全・構造解析・NVH・空力・耐久・最適化・AI サロゲート）のオープンソースツール、データセット、参考資料を集めたリストです。

## Contents

- [Crash & Explicit Dynamics](#crash--explicit-dynamics)
- [Structural FEA (Implicit)](#structural-fea-implicit)
- [NVH & Structural Dynamics](#nvh--structural-dynamics)
- [CFD & Aerodynamics](#cfd--aerodynamics)
- [Pre / Post-processing & Meshing](#pre--post-processing--meshing)
- [Result File Handling (Python)](#result-file-handling-python)
- [Human Body Models & Occupant Safety](#human-body-models--occupant-safety)
- [Optimization & MDO](#optimization--mdo)
- [AI Surrogates & Datasets](#ai-surrogates--datasets)
- [Vehicle Dynamics, EV & System Simulation](#vehicle-dynamics-ev--system-simulation)
- [HPC & Workflow](#hpc--workflow)
- [Commercial Reference (for context)](#commercial-reference-for-context)
- [Standards, Regulations & Communities](#standards-regulations--communities)
- [Japan](#japan)
- [Related Lists](#related-lists)
- [My Awesome Lists](#my-awesome-lists)
- [Contributing](#contributing)
- [License](#license)

## Crash & Explicit Dynamics

- [OpenRadioss](https://github.com/OpenRadioss/OpenRadioss) - Open-source (AGPL) explicit dynamics solver for crash, impact, and high-speed events; can read LS-DYNA-format input. ![stars](https://img.shields.io/github/stars/OpenRadioss/OpenRadioss?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/OpenRadioss/OpenRadioss?style=flat-square)
- [OpenCourant](https://github.com/OpenCourant/OpenCourant) - Open-source explicit FE solver described as the community continuation of OpenRadioss (AGPL v3); project site [opencourant.org](https://opencourant.org) — verify project status. ![stars](https://img.shields.io/github/stars/OpenCourant/OpenCourant?style=flat-square) ![release](https://img.shields.io/github/release-date/OpenCourant/OpenCourant?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/OpenCourant/OpenCourant?style=flat-square)
- [Kratos Multiphysics](https://github.com/KratosMultiphysics/Kratos) - Multiphysics framework with structural mechanics and contact. ![stars](https://img.shields.io/github/stars/KratosMultiphysics/Kratos?style=flat-square) ![release](https://img.shields.io/github/release-date/KratosMultiphysics/Kratos?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/KratosMultiphysics/Kratos?style=flat-square)
- [Public LS-DYNA Model Archive (CCSA, formerly NCAC)](https://www.ccsa.gmu.edu/models/) - Free full-vehicle FE models for crash simulation (e.g. 2007 Chevrolet Silverado, 2010 Toyota Yaris). Check each model's terms before use.

## Structural FEA (Implicit)

- [Code_Aster](https://code-aster.org) - Large open-source structural / thermal solver (EDF).
- [CalculiX](https://www.calculix.de) - 3D structural FEA with Abaqus-like input format.
- [Elmer FEM](https://www.elmerfem.org) - Multiphysics FEM including structural, acoustics, and thermal.
- [FEniCS](https://fenicsproject.org) - Python / C++ platform for solving PDEs by FEM.
- [MOOSE](https://mooseframework.inl.gov) - Multiphysics object-oriented simulation environment.

## NVH & Structural Dynamics

- [SDyPy](https://github.com/sdypy) - Structural dynamics in Python (experimental modal analysis, FRF, UFF I/O).
- Code_Aster and Elmer (above) support modal and harmonic response analysis.
- [pyva](https://pyva.eu) - Python toolbox for vibroacoustics: FEM, statistical energy analysis (SEA), and hybrid FEM/SEA.
- [Bempp-cl](https://bempp.com) - Python boundary element library for acoustics (Helmholtz), electrostatics, and electromagnetics; includes acoustics tutorials. [Source](https://github.com/bempp/bempp-cl). ![stars](https://img.shields.io/github/stars/bempp/bempp-cl?style=flat-square) ![release](https://img.shields.io/github/release-date/bempp/bempp-cl?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/bempp/bempp-cl?style=flat-square)
- <!-- TODO: transfer path analysis, order analysis (no mature open-source library found; results were mostly MATLAB / commercial) -->

## CFD & Aerodynamics

- [OpenFOAM (openfoam.org)](https://openfoam.org) / [OpenFOAM (openfoam.com)](https://www.openfoam.com) - Open-source CFD toolbox; widely used for external vehicle aerodynamics.
- [SU2](https://su2code.github.io) - Multiphysics CFD and design optimization suite.
- <!-- TODO: thermal management, underhood, aeroacoustics, lattice Boltzmann solvers -->

## Pre / Post-processing & Meshing

- [Gmsh](https://gmsh.info) - Mesh generator with built-in CAD engine.
- [SALOME](https://www.salome-platform.org) - Pre / post-processing platform, commonly paired with Code_Aster.
- [ParaView](https://www.paraview.org) - Scientific visualization and post-processing.
- [FreeCAD](https://www.freecad.org) - Parametric 3D CAD with FEM workbench.
- [meshio](https://github.com/nschloe/meshio) - Mesh file I/O across many formats. ![stars](https://img.shields.io/github/stars/nschloe/meshio?style=flat-square) ![release](https://img.shields.io/github/release-date/nschloe/meshio?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/nschloe/meshio?style=flat-square)
- [PyVista](https://github.com/pyvista/pyvista) - Python interface to VTK for mesh analysis and plotting. ![stars](https://img.shields.io/github/stars/pyvista/pyvista?style=flat-square) ![release](https://img.shields.io/github/release-date/pyvista/pyvista?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/pyvista/pyvista?style=flat-square)

## Result File Handling (Python)

- [lasso-python](https://github.com/open-lasso-python/lasso-python) - Python library for reading and processing LS-DYNA result data (e.g. d3plot). ![stars](https://img.shields.io/github/stars/open-lasso-python/lasso-python?style=flat-square) ![release](https://img.shields.io/github/release-date/open-lasso-python/lasso-python?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/open-lasso-python/lasso-python?style=flat-square)
- [PyDyna](https://github.com/ansys/pydyna) - Python tooling for LS-DYNA keyword files and workflows. ![stars](https://img.shields.io/github/stars/ansys/pydyna?style=flat-square) ![release](https://img.shields.io/github/release-date/ansys/pydyna?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/ansys/pydyna?style=flat-square)
- [pyNastran](https://github.com/SteveDoyle2/pyNastran) - Python interface for Nastran BDF / OP2 / OP4 files, with a viewer GUI. ![stars](https://img.shields.io/github/stars/SteveDoyle2/pyNastran?style=flat-square) ![release](https://img.shields.io/github/release-date/SteveDoyle2/pyNastran?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/SteveDoyle2/pyNastran?style=flat-square)
- [pylife-odbclient](https://pypi.org/project/pylife-odbclient/) - Reads Abaqus ODB from Python 3 via the Abaqus Python engine. Note: ODB is not an open format, so an Abaqus installation is still required; no license-free reader was found.

## Human Body Models & Occupant Safety

- [THUMS (Toyota)](https://www.toyota.co.jp/thums/) - Total Human Model for Safety; availability and license terms apply.
- [VIVA+ Human Body Models](https://vivaplus.readthedocs.io/) - Open FE human body models (average female and male, seated and standing) under LGPL v3; hosted on the [OpenVT platform](https://openvt.eu).
- <!-- TODO: open dummy (ATD) models -->

## Optimization & MDO

- [OpenMDAO](https://openmdao.org) - Framework for multidisciplinary analysis and optimization.
- [pymoo](https://pymoo.org) - Multi-objective optimization in Python.
- [Optuna](https://optuna.org) - Hyperparameter / black-box optimization framework.
- [Swan (CIMNE)](https://github.com/SwanLab/Swan) - Topology optimization software in MATLAB for 2D / 3D problems with density or level-set design variables. ![stars](https://img.shields.io/github/stars/SwanLab/Swan?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/SwanLab/Swan?style=flat-square)
- [TopOpt (Python)](https://github.com/zfergus/topopt/) - Python library for density-based topology optimization (SIMP, MMA); early-stage. ![stars](https://img.shields.io/github/stars/zfergus/topopt?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/zfergus/topopt?style=flat-square)
- [TopOpt.jl](https://github.com/JuliaTopOpt/TopOpt.jl) - Topology optimization package in Julia: truss and continuum domains, differentiable functions, interactive visualization. ![stars](https://img.shields.io/github/stars/JuliaTopOpt/TopOpt.jl?style=flat-square) ![release](https://img.shields.io/github/release-date/JuliaTopOpt/TopOpt.jl?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/JuliaTopOpt/TopOpt.jl?style=flat-square)
- [GridapTopOpt.jl](https://github.com/zjwegert/GridapTopOpt.jl) - Scalable Julia toolbox for level-set topology optimization (distributed computing, automatic differentiation). ![stars](https://img.shields.io/github/stars/zjwegert/GridapTopOpt.jl?style=flat-square) ![release](https://img.shields.io/github/release-date/zjwegert/GridapTopOpt.jl?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/zjwegert/GridapTopOpt.jl?style=flat-square)
- [FEniCS 55-line topology optimization](https://arxiv.org/abs/2012.08208) - Compact FEniCS implementation for 2D / 3D SIMP, with code.
- [FEniCS TopOpt Foam](https://github.com/diego-hayashi/fenics_topopt_foam) - Fluid topology optimization coupling OpenFOAM and FEniCS/dolfin-adjoint (relevant to thermal / flow-path design). ![stars](https://img.shields.io/github/stars/diego-hayashi/fenics_topopt_foam?style=flat-square) ![release](https://img.shields.io/github/release-date/diego-hayashi/fenics_topopt_foam?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/diego-hayashi/fenics_topopt_foam?style=flat-square)

## AI Surrogates & Datasets

- [NVIDIA PhysicsNeMo](https://github.com/NVIDIA/physicsnemo) - Framework for physics-ML models (formerly Modulus). ![stars](https://img.shields.io/github/stars/NVIDIA/physicsnemo?style=flat-square) ![release](https://img.shields.io/github/release-date/NVIDIA/physicsnemo?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/NVIDIA/physicsnemo?style=flat-square)
- [PhysicsNeMo crash example](https://github.com/NVIDIA/physicsnemo/tree/main/examples/structural_mechanics) - Crash-dynamics surrogates (MeshGraphNet, Transolver, GeoTransolver) with LS-DYNA data preprocessing; see also the paper [arXiv:2510.15201](https://arxiv.org/abs/2510.15201).
- [CarCrashNet](https://github.com/Mohamedelrefaie/CarCrashNet) - Open benchmark for data-driven structural crash simulation: 14,000+ bumper-beam impacts and 825 full-vehicle crashes (Neon, Yaris, Silverado), generated with an OpenRadioss workflow. ![stars](https://img.shields.io/github/stars/Mohamedelrefaie/CarCrashNet?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Mohamedelrefaie/CarCrashNet?style=flat-square)
- [SHIFT-Crash](https://huggingface.co/datasets/luminary-shift/SHIFT-Crash) - 5,000+ frontal crash simulations of a parametrically morphed 2010 Toyota Yaris (CC-BY-NC-4.0; access requires agreeing to share contact info).
- [DrivAerNet / DrivAerNet++](https://github.com/Mohamedelrefaie/DrivAerNet) - 8,000 car designs with CFD results for aerodynamic ML (NeurIPS 2024); about 39 TB, data license CC BY-NC 4.0 (non-commercial), code under MIT. ![stars](https://img.shields.io/github/stars/Mohamedelrefaie/DrivAerNet?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Mohamedelrefaie/DrivAerNet?style=flat-square)
- <!-- TODO: reduced-order models, occupant / pedestrian ML datasets -->

## Vehicle Dynamics, EV & System Simulation

- [OpenModelica](https://openmodelica.org) - Open-source Modelica environment for system-level simulation.
- [PyBaMM](https://pybamm.org) - Battery modelling in Python.
- [CARLA](https://carla.org) - Open-source driving simulator.
- [esmini](https://github.com/esmini/esmini) - OpenSCENARIO player. ![stars](https://img.shields.io/github/stars/esmini/esmini?style=flat-square) ![release](https://img.shields.io/github/release-date/esmini/esmini?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/esmini/esmini?style=flat-square)
- [CommonRoad](https://commonroad.in.tum.de) - Benchmarks for motion planning of vehicles.

## HPC & Workflow

- [OpenFOAM Slurm examples (Pawsey)](https://pawsey.atlassian.net/wiki/x/HFcYAw) - Example Slurm batch scripts for OpenFOAM, including pre / post-processing.
- [OpenFOAM official Apptainer image with site MPI on Slurm (CIQ)](https://ciq.com/blog/integrating-site-specific-mpi-with-an-openfoam-official-apptainer-image-on-slurm-managed-hpc-environments/) - Swapping in the site's OpenMPI so containerized OpenFOAM runs under Slurm.
- [HPC Wiki: SLURM](https://hpc-wiki.info/hpc/SLURM) - General Slurm job script patterns (OpenMP, MPI, job arrays) to adapt for CAE solvers.
- [CalculiX on multiple nodes (forum)](https://calculix.discourse.group/t/can-calculix-run-across-multiple-nodes/1316) - Discussion of CalculiX scaling: mainly multi-threaded, MPI use is limited.
- [OpenRadioss HPC benchmark models](https://openradioss.atlassian.net/wiki/spaces/OPENRADIOSS/pages/47546369/HPC+Benchmark+Models) - Large crash benchmark models (e.g. 10M-element Taurus) for scaling tests.
- <!-- TODO: Slurm templates for OpenRadioss / Code_Aster (no solid public template found yet) -->
- <!-- TODO: simulation data management / PLM-lite, result databases -->

## Commercial Reference (for context)

Listed only to show common industry tooling; not endorsements.

- [Ansys LS-DYNA](https://lsdyna.ansys.com) - De facto standard explicit solver for crash.
- <!-- TODO: Altair HyperWorks / Radioss, MSC Nastran, Abaqus, Star-CCM+ — add official product pages -->

## Standards, Regulations & Communities

- [Euro NCAP](https://www.euroncap.com) - Vehicle safety assessment protocols.
- [NHTSA](https://www.nhtsa.gov) - U.S. vehicle safety regulation and crash test data.
- [NAFEMS](https://www.nafems.org) - Engineering simulation community and best practices.
- [ASAM](https://www.asam.net) - Simulation and testing standards (OpenDRIVE, OpenSCENARIO, etc.).

## Japan

- [JSAE (自動車技術会)](https://www.jsae.or.jp) - Society of Automotive Engineers of Japan.
- [FrontISTR](https://www.frontistr.com) - Japan-developed open-source large-scale parallel structural solver (static / dynamic, eigenvalue, frequency response, heat conduction) — verify URL.
- <!-- TODO: JP-language resources, community events, domestic open-data -->

## Related Lists

Other awesome lists around automotive topics. None of them focuses on automotive CAE (crash, NVH, structural, aerodynamics); this list aims to fill that gap.

**Automotive software & electronics**
- [awesome-automotive](https://github.com/Marcin214/awesome-automotive) - Automotive engineering resources (AUTOSAR, CAN, CAPL, FlexRay). ![stars](https://img.shields.io/github/stars/Marcin214/awesome-automotive?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Marcin214/awesome-automotive?style=flat-square)
- [Awesome-Automotive (ajay-bhojani)](https://github.com/ajay-bhojani/Awesome-Automotive) - Tools, blogs, and sources for automotive engineering. ![stars](https://img.shields.io/github/stars/ajay-bhojani/Awesome-Automotive?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/ajay-bhojani/Awesome-Automotive?style=flat-square)
- [Awesome-Automotive-Electronics](https://github.com/Leohc92/Awesome-Automotive-Electronics) - Automotive electronic systems knowledge and software. ![stars](https://img.shields.io/github/stars/Leohc92/Awesome-Automotive-Electronics?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Leohc92/Awesome-Automotive-Electronics?style=flat-square)
- [awesome-sdv](https://github.com/yzy-comfortuni/awesome-sdv) - Software-defined vehicle resources (AUTOSAR, Rust, DDS, SIL/HIL, OTA); Chinese / English. ![stars](https://img.shields.io/github/stars/yzy-comfortuni/awesome-sdv?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/yzy-comfortuni/awesome-sdv?style=flat-square)

**Security & vehicle buses**
- [awesome-vehicle-security](https://github.com/jaredthecoder/awesome-vehicle-security) - Vehicle security and car hacking. ![stars](https://img.shields.io/github/stars/jaredthecoder/awesome-vehicle-security?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/jaredthecoder/awesome-vehicle-security?style=flat-square)
- [awesome-canbus](https://github.com/iDoka/awesome-canbus) - CAN bus tools, hardware, and resources. ![stars](https://img.shields.io/github/stars/iDoka/awesome-canbus?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/iDoka/awesome-canbus?style=flat-square)
- [awesome-automotive-can-id](https://github.com/iDoka/awesome-automotive-can-id) - CAN IDs and payloads for various car models. ![stars](https://img.shields.io/github/stars/iDoka/awesome-automotive-can-id?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/iDoka/awesome-automotive-can-id?style=flat-square)
- [awesome-linbus](https://github.com/iDoka/awesome-linbus) - LIN bus tools and resources. ![stars](https://img.shields.io/github/stars/iDoka/awesome-linbus?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/iDoka/awesome-linbus?style=flat-square)
- [awesome-automotive-security](https://github.com/hexsecs/awesome-automotive-security) - Automotive security. ![stars](https://img.shields.io/github/stars/hexsecs/awesome-automotive-security?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/hexsecs/awesome-automotive-security?style=flat-square)
- [AwesomeSafetyAndSecurityForAuto](https://github.com/tengfeiwork/AwesomeSafetyAndSecurityForAuto) - Functional safety, SOTIF, and cybersecurity repositories. ![stars](https://img.shields.io/github/stars/tengfeiwork/AwesomeSafetyAndSecurityForAuto?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/tengfeiwork/AwesomeSafetyAndSecurityForAuto?style=flat-square)

**Autonomous driving & robotics**
- [awesome-robotic-tooling](https://github.com/Ly0n/awesome-robotic-tooling) - Tooling for robotics and autonomous driving (ROS, lidar, SLAM). ![stars](https://img.shields.io/github/stars/Ly0n/awesome-robotic-tooling?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/Ly0n/awesome-robotic-tooling?style=flat-square)
- [Awesome-Autonomous-Driving (autodriving-heart)](https://github.com/autodriving-heart/Awesome-Autonomous-Driving) - Autonomous driving resources. ![stars](https://img.shields.io/github/stars/autodriving-heart/Awesome-Autonomous-Driving?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/autodriving-heart/Awesome-Autonomous-Driving?style=flat-square)
- [Awesome-Autonomous-Driving (autonomousdrivingkr)](https://github.com/autonomousdrivingkr/Awesome-Autonomous-Driving) - Autonomous driving resources. ![stars](https://img.shields.io/github/stars/autonomousdrivingkr/Awesome-Autonomous-Driving?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/autonomousdrivingkr/Awesome-Autonomous-Driving?style=flat-square)
- [awesome-end-to-end-autonomous-driving](https://github.com/opendilab/awesome-end-to-end-autonomous-driving) - End-to-end autonomous driving. ![stars](https://img.shields.io/github/stars/opendilab/awesome-end-to-end-autonomous-driving?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/opendilab/awesome-end-to-end-autonomous-driving?style=flat-square)
- [awesome-vla-for-ad](https://github.com/worldbench/awesome-vla-for-ad) - Vision-language-action models for autonomous driving. ![stars](https://img.shields.io/github/stars/worldbench/awesome-vla-for-ad?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/worldbench/awesome-vla-for-ad?style=flat-square)

**EV**
- [awesome-ev-charging](https://github.com/juherr/awesome-ev-charging) - Tools for electric vehicle charging. ![stars](https://img.shields.io/github/stars/juherr/awesome-ev-charging?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/juherr/awesome-ev-charging?style=flat-square)

## My Awesome Lists

Awesome lists by the same author ([shvyac](https://github.com/shvyac)).

**CAE & engineering**
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) - Awesome lists about CAD / CAE and related topics. ![stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-cad-cae?style=flat-square)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) - Open-source solvers: FEM, BEM, CFD, dynamics, particles, acoustics, combustion, quantum, scientific computing. ![stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-open-source-solvers?style=flat-square)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) - CAE tools without a traditional mesh: particle methods, lattice Boltzmann, MPM, peridynamics, isogeometric analysis, AI surrogates. ![stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-meshless-cae?style=flat-square)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) - AI-powered tools for mechanical engineering: CAD, simulation, generative design, topology optimization, manufacturing. ![stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat-square)
- [cae_tools](https://github.com/shvyac/cae_tools) - Tech info on CAE, systems engineering, requirements and ALM tools. ![stars](https://img.shields.io/github/stars/shvyac/cae_tools?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/cae_tools?style=flat-square)

**AI & MCP**
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) - Local LLM resources: inference engines, apps and chat UIs, local-first RAG / agents, fine-tuning, model selection for your hardware. ![stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-local-llm?style=flat-square)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) - AI / LLM / MCP tools for OSINT: agents, MCP servers, situational-awareness dashboards, GEOINT, Japan-focused data. ![stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-osint-ai?style=flat-square)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) - Open-source CMS and the tools to drive them from AI and MCP. ![stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-cms-ai?style=flat-square)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) - Using AI with Redmine: AI plugins, MCP servers, local LLM setups, automation, GitHub integration. ![stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-redmine-ai?style=flat-square)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) - Open-source tools for hierarchical requirement trees (whole vehicle / company IT), as-built sync, traceability, with AI and MCP. ![stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-requirements-system-ai?style=flat-square)

**IT, dashboards & security**
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) - Open-source dashboard and data-visualization tools like Grafana. ![stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-dashboards-visualization?style=flat-square)
- [awesome-ai-powered-executive-dashboards](https://github.com/shvyac/awesome-ai-powered-executive-dashboards) - AI-powered management and organizational transformation tools, services, and articles (Japanese). ![stars](https://img.shields.io/github/stars/shvyac/awesome-ai-powered-executive-dashboards?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-ai-powered-executive-dashboards?style=flat-square)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) - Open-source tools, templates, and AI integrations for operating an ISO/IEC 27001 ISMS. ![stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-iso27001-isms-tools?style=flat-square)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) - Japanese-first resources on Microsoft Azure AI, Dynamics 365, Power Platform, Identity, and Security. ![stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-azure-ai-dynamics365-security?style=flat-square)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) - Online services, languages, IDEs, and other interesting topics. ![stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-online-services?style=flat-square)

**Hobbies & others**
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) - Amateur / ham radio resources: licensing, band plans, SDR, digital modes, antennas, contests, satellites, APRS, JARL. ![stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-hamradio?style=flat-square)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) - Resources for Ballroom Dance, focused on the 10 International Style dances. ![stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-ballroom-dance?style=flat-square)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) - Software for audio processing, music visualization, and sound analysis. ![stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-audio-softwares?style=flat-square)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) - AI-made unidentified artists found on Apple Music and Spotify, grouped by style (Japanese). ![stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-ghost-artists?style=flat-square)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) - Curated links for developing with M5Stack devices using Arduino / PlatformIO. ![stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-m5stack-arduino?style=flat-square)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) - Maps / GIS tools and resources, including Japan-focused geospatial services. ![stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-map-gis?style=flat-square)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) - Stock / markets / trading resources: market-data APIs, charting, backtesting, filings, quant tooling, JPX / EDINET / J-Quants. ![stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-trading-stock?style=flat-square)
- [awesome-quantum](https://github.com/shvyac/awesome-quantum) - Quantum-related awesome list. ![stars](https://img.shields.io/github/stars/shvyac/awesome-quantum?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/shvyac/awesome-quantum?style=flat-square)

## Contributing

Pull requests welcome. Please:

1. Link to the official project page or repository (avoid blog mirrors).
2. Keep one line per entry: `[Name](URL) - Short description.` followed by badges when the entry is a GitHub repository (see the update rule below).
3. Prefer actively maintained projects; mark archived ones.
4. Keep entries alphabetical within a section where practical.

### Update Rule

Every entry that points to a GitHub repository carries live [shields.io](https://shields.io) badges at the end of its line, in this order: stars, release date, last commit.

```markdown
![stars](https://img.shields.io/github/stars/OWNER/REPO?style=flat-square) ![release](https://img.shields.io/github/release-date/OWNER/REPO?style=flat-square) ![last commit](https://img.shields.io/github/last-commit/OWNER/REPO?style=flat-square)
```

- Replace `OWNER/REPO` with the repository path. The badges refresh automatically; no manual updates are needed.
- **Release date is shown only if the repository has a published GitHub release.** If no release is found (check `https://github.com/OWNER/REPO/releases`), leave the release badge out entirely (blank) and keep only stars and last commit. Re-check when the repository publishes its first release, then add the release badge.
- Use the repository root, not a subdirectory link. Entries that only link to a subdirectory of a repository listed elsewhere get no badges.
- Entries not hosted on GitHub (project sites, other dataset hosts, papers, forums) and organization-only links get no badges.
- When reviewing entries, check the last-commit badge. Mark or remove entries that look inactive or are archived.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
