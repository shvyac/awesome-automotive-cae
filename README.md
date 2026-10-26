# Awesome Automotive CAE [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of open-source tools, datasets, and references for **automotive CAE** — crash safety, structural FEA, NVH, CFD / aerodynamics, durability, optimization, and AI surrogates. Prefer durable official / project URLs.
>
> 自動車 CAE（衝突安全・構造解析・NVH・空力・耐久・最適化・AI サロゲート）のオープンソースツール、データセット、参考資料を集めたリストです。

## Related Lists

**CAE (same author)**
[awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ・ [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ・ [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ・ [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering)

**Automotive software & electronics**
- [awesome-automotive](https://github.com/Marcin214/awesome-automotive) - Automotive engineering resources (AUTOSAR, CAN, CAPL, FlexRay).
- [Awesome-Automotive (ajay-bhojani)](https://github.com/ajay-bhojani/Awesome-Automotive) - Tools, blogs, and sources for automotive engineering.
- [Awesome-Automotive-Electronics](https://github.com/Leohc92/Awesome-Automotive-Electronics) - Automotive electronic systems knowledge and software.
- [awesome-sdv](https://github.com/yzy-comfortuni/awesome-sdv) - Software-defined vehicle resources (AUTOSAR, Rust, DDS, SIL/HIL, OTA); Chinese / English.

**Security & vehicle buses**
- [awesome-vehicle-security](https://github.com/jaredthecoder/awesome-vehicle-security) - Vehicle security and car hacking.
- [awesome-canbus](https://github.com/iDoka/awesome-canbus) - CAN bus tools, hardware, and resources.
- [awesome-automotive-can-id](https://github.com/iDoka/awesome-automotive-can-id) - CAN IDs and payloads for various car models.
- [awesome-linbus](https://github.com/iDoka/awesome-linbus) - LIN bus tools and resources.
- [awesome-automotive-security](https://github.com/hexsecs/awesome-automotive-security) - Automotive security.
- [AwesomeSafetyAndSecurityForAuto](https://github.com/tengfeiwork/AwesomeSafetyAndSecurityForAuto) - Functional safety, SOTIF, and cybersecurity repositories.

**Autonomous driving & robotics**
- [awesome-robotic-tooling](https://github.com/Ly0n/awesome-robotic-tooling) - Tooling for robotics and autonomous driving (ROS, lidar, SLAM).
- [Awesome-Autonomous-Driving (autodriving-heart)](https://github.com/autodriving-heart/Awesome-Autonomous-Driving) - Autonomous driving resources.
- [Awesome-Autonomous-Driving (autonomousdrivingkr)](https://github.com/autonomousdrivingkr/Awesome-Autonomous-Driving) - Autonomous driving resources.
- [awesome-end-to-end-autonomous-driving](https://github.com/opendilab/awesome-end-to-end-autonomous-driving) - End-to-end autonomous driving.
- [awesome-vla-for-ad](https://github.com/worldbench/awesome-vla-for-ad) - Vision-language-action models for autonomous driving.

**EV**
- [awesome-ev-charging](https://github.com/juherr/awesome-ev-charging) - Tools for electric vehicle charging.

None of the above focuses on automotive CAE (crash, NVH, structural, aerodynamics); this list aims to fill that gap.

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
- [Contributing](#contributing)

## Crash & Explicit Dynamics

- [OpenRadioss](https://github.com/OpenRadioss/OpenRadioss) - Open-source (AGPL) explicit dynamics solver for crash, impact, and high-speed events; can read LS-DYNA-format input.
- [OpenCourant](https://github.com/OpenCourant/OpenCourant) - Open-source explicit FE solver described as the community continuation of OpenRadioss (AGPL v3); project site [opencourant.org](https://opencourant.org) — verify project status.
- [Kratos Multiphysics](https://github.com/KratosMultiphysics/Kratos) - Multiphysics framework with structural mechanics and contact.
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
- [Bempp-cl](https://bempp.com) - Python boundary element library for acoustics (Helmholtz), electrostatics, and electromagnetics; includes acoustics tutorials. [Source](https://github.com/bempp/bempp-cl).
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
- [meshio](https://github.com/nschloe/meshio) - Mesh file I/O across many formats.
- [PyVista](https://github.com/pyvista/pyvista) - Python interface to VTK for mesh analysis and plotting.

## Result File Handling (Python)

- [lasso-python](https://github.com/open-lasso-python/lasso-python) - Python library for reading and processing LS-DYNA result data (e.g. d3plot).
- [PyDyna](https://github.com/ansys/pydyna) - Python tooling for LS-DYNA keyword files and workflows.
- [pyNastran](https://github.com/SteveDoyle2/pyNastran) - Python interface for Nastran BDF / OP2 / OP4 files, with a viewer GUI.
- [pylife-odbclient](https://pypi.org/project/pylife-odbclient/) - Reads Abaqus ODB from Python 3 via the Abaqus Python engine. Note: ODB is not an open format, so an Abaqus installation is still required; no license-free reader was found.

## Human Body Models & Occupant Safety

- [THUMS (Toyota)](https://www.toyota.co.jp/thums/) - Total Human Model for Safety; availability and license terms apply.
- [VIVA+ Human Body Models](https://vivaplus.readthedocs.io/) - Open FE human body models (average female and male, seated and standing) under LGPL v3; hosted on the [OpenVT platform](https://openvt.eu).
- <!-- TODO: open dummy (ATD) models -->

## Optimization & MDO

- [OpenMDAO](https://openmdao.org) - Framework for multidisciplinary analysis and optimization.
- [pymoo](https://pymoo.org) - Multi-objective optimization in Python.
- [Optuna](https://optuna.org) - Hyperparameter / black-box optimization framework.
- [Swan (CIMNE)](https://github.com/SwanLab/Swan) - Topology optimization software in MATLAB for 2D / 3D problems with density or level-set design variables.
- [TopOpt (Python)](https://github.com/zfergus/topopt/) - Python library for density-based topology optimization (SIMP, MMA); early-stage.
- [TopOpt.jl](https://github.com/JuliaTopOpt/TopOpt.jl) - Topology optimization package in Julia: truss and continuum domains, differentiable functions, interactive visualization.
- [GridapTopOpt.jl](https://github.com/zjwegert/GridapTopOpt.jl) - Scalable Julia toolbox for level-set topology optimization (distributed computing, automatic differentiation).
- [FEniCS 55-line topology optimization](https://arxiv.org/abs/2012.08208) - Compact FEniCS implementation for 2D / 3D SIMP, with code.
- [FEniCS TopOpt Foam](https://github.com/diego-hayashi/fenics_topopt_foam) - Fluid topology optimization coupling OpenFOAM and FEniCS/dolfin-adjoint (relevant to thermal / flow-path design).

## AI Surrogates & Datasets

- [NVIDIA PhysicsNeMo](https://github.com/NVIDIA/physicsnemo) - Framework for physics-ML models (formerly Modulus).
- [PhysicsNeMo crash example](https://github.com/NVIDIA/physicsnemo/tree/main/examples/structural_mechanics) - Crash-dynamics surrogates (MeshGraphNet, Transolver, GeoTransolver) with LS-DYNA data preprocessing; see also the paper [arXiv:2510.15201](https://arxiv.org/abs/2510.15201).
- [CarCrashNet](https://github.com/Mohamedelrefaie/CarCrashNet) - Open benchmark for data-driven structural crash simulation: 14,000+ bumper-beam impacts and 825 full-vehicle crashes (Neon, Yaris, Silverado), generated with an OpenRadioss workflow.
- [SHIFT-Crash](https://huggingface.co/datasets/luminary-shift/SHIFT-Crash) - 5,000+ frontal crash simulations of a parametrically morphed 2010 Toyota Yaris (CC-BY-NC-4.0; access requires agreeing to share contact info).
- [DrivAerNet / DrivAerNet++](https://github.com/Mohamedelrefaie/DrivAerNet) - 8,000 car designs with CFD results for aerodynamic ML (NeurIPS 2024); about 39 TB, data license CC BY-NC 4.0 (non-commercial), code under MIT.
- <!-- TODO: reduced-order models, occupant / pedestrian ML datasets -->

## Vehicle Dynamics, EV & System Simulation

- [OpenModelica](https://openmodelica.org) - Open-source Modelica environment for system-level simulation.
- [PyBaMM](https://pybamm.org) - Battery modelling in Python.
- [CARLA](https://carla.org) - Open-source driving simulator.
- [esmini](https://github.com/esmini/esmini) - OpenSCENARIO player.
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

## Contributing

Pull requests welcome. Please:

1. Link to the official project page or repository (avoid blog mirrors).
2. Keep one line per entry: `[Name](URL) - Short description.`
3. Prefer actively maintained projects; mark archived ones.
4. Keep entries alphabetical within a section where practical.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
