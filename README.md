# Awesome Automotive CAE [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of open-source tools, datasets, and references for **automotive CAE** — crash safety, structural FEA, NVH, CFD / aerodynamics, durability, optimization, and AI surrogates. Prefer durable official / project URLs.
>
> 自動車 CAE（衝突安全・構造解析・NVH・空力・耐久・最適化・AI サロゲート）のオープンソースツール、データセット、参考資料を集めたリストです。
>
> ⭐ badges show live GitHub star counts (via shields.io); release badges show the date of the latest GitHub release (YYYY/MM/DD, as of the last refresh); last-commit badges show live commit activity (via shields.io).

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
- [Powertrain & Engine Dynamics](#powertrain--engine-dynamics)
- [HPC & Workflow](#hpc--workflow)
- [Commercial Reference (for context)](#commercial-reference-for-context)
- [Standards, Regulations & Communities](#standards-regulations--communities)
- [Japan](#japan)
- [Related Lists](#related-lists)
- [Contributing](#contributing)
- [License](#license)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

## Crash & Explicit Dynamics

- [OpenCourant](https://github.com/OpenCourant/OpenCourant) - Open-source (AGPL v3) explicit FE solver for crash, impact, and high-speed events; community continuation of OpenRadioss, forked from its last open-source code base after Siemens discontinued OpenRadioss and deleted its repository on 2026-10-01. Incubating at the Rocky Enterprise Software Foundation; site [opencourant.org](https://opencourant.org). ![GitHub stars](https://img.shields.io/github/stars/OpenCourant/OpenCourant?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F11-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/OpenCourant/OpenCourant?style=flat)
- [Kratos Multiphysics](https://github.com/KratosMultiphysics/Kratos) - Multiphysics framework with structural mechanics and contact. ![GitHub stars](https://img.shields.io/github/stars/KratosMultiphysics/Kratos?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F06-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/KratosMultiphysics/Kratos?style=flat)
- [Public LS-DYNA Model Archive (CCSA, formerly NCAC)](https://www.ccsa.gmu.edu/models/) - Free full-vehicle FE models for crash simulation (e.g. 2010 Toyota Yaris, 2015 Toyota Camry, 2014 Chevrolet Silverado, 2018 Dodge Ram, 2020 Nissan Rogue). Check each model's terms before use.

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
- [Bempp-cl](https://bempp.com) - Python boundary element library for acoustics (Helmholtz), electrostatics, and electromagnetics; includes acoustics tutorials. [Source](https://github.com/bempp/bempp-cl). ![GitHub stars](https://img.shields.io/github/stars/bempp/bempp-cl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F04%2F01-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/bempp/bempp-cl?style=flat)
- <!-- TODO: transfer path analysis, order analysis (no mature open-source library found; results were mostly MATLAB / commercial) -->

## CFD & Aerodynamics

- [OpenFOAM (openfoam.org)](https://openfoam.org) / [OpenFOAM (openfoam.com)](https://www.openfoam.com) - Open-source CFD toolbox; widely used for external vehicle aerodynamics.
- [SU2](https://su2code.github.io) - Multiphysics CFD and design optimization suite.
- [libAcoustics](https://github.com/unicfdlab/libAcoustics) ![New](https://img.shields.io/badge/-NEW-red?style=flat) - OpenFOAM function-object library for far-field aeroacoustic noise (Curle and Ffowcs Williams-Hawkings analogies, CFD-BEM coupling); branches for OpenFOAM v2112 and later. ![GitHub stars](https://img.shields.io/github/stars/unicfdlab/libAcoustics?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2022%2F04%2F08-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/unicfdlab/libAcoustics?style=flat)
- [XLB](https://github.com/Autodesk/XLB) ![New](https://img.shields.io/badge/-NEW-red?style=flat) - Differentiable, GPU-accelerated 2D / 3D lattice Boltzmann library in Python (JAX, NVIDIA Warp, Neon backends) for flow simulation and physics-based ML (Apache-2.0). ![GitHub stars](https://img.shields.io/github/stars/Autodesk/XLB?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F20-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Autodesk/XLB?style=flat)
- <!-- TODO: thermal management, underhood -->

## Pre / Post-processing & Meshing

- [Gmsh](https://gmsh.info) - Mesh generator with built-in CAD engine.
- [SALOME](https://www.salome-platform.org) - Pre / post-processing platform, commonly paired with Code_Aster.
- [ParaView](https://www.paraview.org) - Scientific visualization and post-processing.
- [FreeCAD](https://www.freecad.org) - Parametric 3D CAD with FEM workbench.
- [meshio](https://github.com/nschloe/meshio) - Mesh file I/O across many formats. ![GitHub stars](https://img.shields.io/github/stars/nschloe/meshio?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F01%2F31-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/nschloe/meshio?style=flat)
- [PyVista](https://github.com/pyvista/pyvista) - Python interface to VTK for mesh analysis and plotting. ![GitHub stars](https://img.shields.io/github/stars/pyvista/pyvista?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F24-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/pyvista/pyvista?style=flat)

## Result File Handling (Python)

- [lasso-python](https://github.com/open-lasso-python/lasso-python) - Python library for reading and processing LS-DYNA result data (e.g. d3plot). ![GitHub stars](https://img.shields.io/github/stars/open-lasso-python/lasso-python?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F08%2F30-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/open-lasso-python/lasso-python?style=flat)
- [PyDyna](https://github.com/ansys/pydyna) - Python tooling for LS-DYNA keyword files and workflows. ![GitHub stars](https://img.shields.io/github/stars/ansys/pydyna?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F05%2F18-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/ansys/pydyna?style=flat)
- [pyNastran](https://github.com/SteveDoyle2/pyNastran) - Python interface for Nastran BDF / OP2 / OP4 files, with a viewer GUI. ![GitHub stars](https://img.shields.io/github/stars/SteveDoyle2/pyNastran?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F03%2F26-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/SteveDoyle2/pyNastran?style=flat)
- [pylife-odbclient](https://pypi.org/project/pylife-odbclient/) - Reads Abaqus ODB from Python 3 via the Abaqus Python engine. Note: ODB is not an open format, so an Abaqus installation is still required; no license-free reader was found.

## Human Body Models & Occupant Safety

- [THUMS (Toyota)](https://www.toyota.co.jp/thums/) - Total Human Model for Safety; availability and license terms apply.
- [VIVA+ Human Body Models](https://vivaplus.readthedocs.io/) - Open FE human body models (average female and male, seated and standing) under LGPL v3; hosted on the [OpenVT platform](https://openvt.eu).
- <!-- TODO: open dummy (ATD) models -->

## Optimization & MDO

- [OpenMDAO](https://openmdao.org) - Framework for multidisciplinary analysis and optimization.
- [pymoo](https://pymoo.org) - Multi-objective optimization in Python.
- [Optuna](https://optuna.org) - Hyperparameter / black-box optimization framework.
- [Swan (CIMNE)](https://github.com/SwanLab/Swan) - Topology optimization software in MATLAB for 2D / 3D problems with density or level-set design variables. ![GitHub stars](https://img.shields.io/github/stars/SwanLab/Swan?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/SwanLab/Swan?style=flat)
- [TopOpt (Python)](https://github.com/zfergus/topopt/) - Python library for density-based topology optimization (SIMP, MMA); early-stage. ![GitHub stars](https://img.shields.io/github/stars/zfergus/topopt?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/zfergus/topopt?style=flat)
- [TopOpt.jl](https://github.com/JuliaTopOpt/TopOpt.jl) - Topology optimization package in Julia: truss and continuum domains, differentiable functions, interactive visualization. ![GitHub stars](https://img.shields.io/github/stars/JuliaTopOpt/TopOpt.jl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/JuliaTopOpt/TopOpt.jl?style=flat)
- [GridapTopOpt.jl](https://github.com/zjwegert/GridapTopOpt.jl) - Scalable Julia toolbox for level-set topology optimization (distributed computing, automatic differentiation). ![GitHub stars](https://img.shields.io/github/stars/zjwegert/GridapTopOpt.jl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F16-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/zjwegert/GridapTopOpt.jl?style=flat)
- [FEniCS 55-line topology optimization](https://arxiv.org/abs/2012.08208) - Compact FEniCS implementation for 2D / 3D SIMP, with code.
- [FEniCS TopOpt Foam](https://github.com/diego-hayashi/fenics_topopt_foam) - Fluid topology optimization coupling OpenFOAM and FEniCS/dolfin-adjoint (relevant to thermal / flow-path design). ![GitHub stars](https://img.shields.io/github/stars/diego-hayashi/fenics_topopt_foam?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2024%2F08%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/diego-hayashi/fenics_topopt_foam?style=flat)

## AI Surrogates & Datasets

- [NVIDIA PhysicsNeMo](https://github.com/NVIDIA/physicsnemo) - Framework for physics-ML models (formerly Modulus). ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/physicsnemo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/NVIDIA/physicsnemo?style=flat)
- [PhysicsNeMo crash example](https://github.com/NVIDIA/physicsnemo/tree/main/examples/structural_mechanics) - Crash-dynamics surrogates (MeshGraphNet, Transolver, GeoTransolver) with LS-DYNA data preprocessing; see also the paper [arXiv:2510.15201](https://arxiv.org/abs/2510.15201).
- [CarCrashNet](https://github.com/Mohamedelrefaie/CarCrashNet) - Open benchmark for data-driven structural crash simulation: 14,000+ bumper-beam impacts and 825 full-vehicle crashes (Neon, Yaris, Silverado), generated with an OpenRadioss workflow (OpenRadioss is now continued as OpenCourant). ![GitHub stars](https://img.shields.io/github/stars/Mohamedelrefaie/CarCrashNet?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Mohamedelrefaie/CarCrashNet?style=flat)
- [SHIFT-Crash](https://huggingface.co/datasets/luminary-shift/SHIFT-Crash) - 5,000+ frontal crash simulations of a parametrically morphed 2010 Toyota Yaris (CC-BY-NC-4.0; access requires agreeing to share contact info).
- [DrivAerNet / DrivAerNet++](https://github.com/Mohamedelrefaie/DrivAerNet) - 8,000 car designs with CFD results for aerodynamic ML (NeurIPS 2024); about 39 TB, data license CC BY-NC 4.0 (non-commercial), code under MIT. ![GitHub stars](https://img.shields.io/github/stars/Mohamedelrefaie/DrivAerNet?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Mohamedelrefaie/DrivAerNet?style=flat)
- [DrivAerML](https://huggingface.co/datasets/neashton/drivaerml) ![New](https://img.shields.io/badge/-NEW-red?style=flat) - High-fidelity scale-resolving CFD (OpenFOAM) of 500 morphed DrivAer notchback variants (484 public runs, about 31 TB) for road-car aerodynamics ML; CC BY-SA 4.0.
- <!-- TODO: reduced-order models, occupant / pedestrian ML datasets -->

## Vehicle Dynamics, EV & System Simulation

- [OpenModelica](https://openmodelica.org) - Open-source Modelica environment for system-level simulation.
- [PyBaMM](https://pybamm.org) - Battery modelling in Python.
- [CARLA](https://carla.org) - Open-source driving simulator.
- [esmini](https://github.com/esmini/esmini) - OpenSCENARIO player. ![GitHub stars](https://img.shields.io/github/stars/esmini/esmini?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F11%2F25-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/esmini/esmini?style=flat)
- [CommonRoad](https://commonroad.in.tum.de) - Benchmarks for motion planning of vehicles.
- [Project Chrono](https://github.com/projectchrono/chrono) ![New](https://img.shields.io/badge/-NEW-red?style=flat) - C++ multibody and multiphysics dynamics library (BSD-3-Clause); the Chrono::Vehicle module models wheeled and tracked vehicles, tires, suspensions, and terrain. ![GitHub stars](https://img.shields.io/github/stars/projectchrono/chrono?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F04%2F07-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/projectchrono/chrono?style=flat)

## Powertrain & Engine Dynamics

- [OpenFOAM ICengines](https://github.com/OpenFOAM/ICengines) - Example cases for IC-engine CFD in OpenFOAM-dev: piston and valve motion with the `multiValveEngine` mesh mover and mesh-to-mesh mapping. ![GitHub stars](https://img.shields.io/github/stars/OpenFOAM/ICengines?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F05%2F26-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/OpenFOAM/ICengines?style=flat)
- [openTorsion](https://github.com/Aalto-Arotor/openTorsion) - Python library for torsional vibration of shaft lines (e.g. crankshafts): FE models, natural frequencies, mode shapes, forced response, and time-stepping. ![GitHub stars](https://img.shields.io/github/stars/Aalto-Arotor/openTorsion?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Aalto-Arotor/openTorsion?style=flat)
- [Slider-Crank](https://github.com/JAlcocerT/Slider-Crank) - Python notebooks and web apps (Streamlit / Dash) for slider-crank kinematics: piston position, offset effect, and connecting-rod angle over the crank cycle (GPL-3.0). ![GitHub stars](https://img.shields.io/github/stars/JAlcocerT/Slider-Crank?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/JAlcocerT/Slider-Crank?style=flat)

## HPC & Workflow

- [OpenFOAM Slurm examples (Pawsey)](https://pawsey.atlassian.net/wiki/x/HFcYAw) - Example Slurm batch scripts for OpenFOAM, including pre / post-processing.
- [OpenFOAM official Apptainer image with site MPI on Slurm (CIQ)](https://ciq.com/blog/integrating-site-specific-mpi-with-an-openfoam-official-apptainer-image-on-slurm-managed-hpc-environments/) - Swapping in the site's OpenMPI so containerized OpenFOAM runs under Slurm.
- [HPC Wiki: SLURM](https://hpc-wiki.info/hpc/SLURM) - General Slurm job script patterns (OpenMP, MPI, job arrays) to adapt for CAE solvers.
- [CalculiX on multiple nodes (forum)](https://calculix.discourse.group/t/can-calculix-run-across-multiple-nodes/1316) - Discussion of CalculiX scaling: mainly multi-threaded, MPI use is limited.
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
- [FrontISTR](https://www.frontistr.com) - Japan-developed open-source large-scale parallel structural solver (static / dynamic, eigenvalue, frequency response, heat conduction), maintained by FrontISTR Commons; v6.0 released Oct 2026.
- <!-- TODO: JP-language resources, community events, domestic open-data -->

## Related Lists

Other awesome lists around automotive topics. None of them focuses on automotive CAE (crash, NVH, structural, aerodynamics); this list aims to fill that gap.

**Automotive software & electronics**
- [awesome-automotive](https://github.com/Marcin214/awesome-automotive) - Automotive engineering resources (AUTOSAR, CAN, CAPL, FlexRay). ![GitHub stars](https://img.shields.io/github/stars/Marcin214/awesome-automotive?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Marcin214/awesome-automotive?style=flat)
- [Awesome-Automotive (ajay-bhojani)](https://github.com/ajay-bhojani/Awesome-Automotive) - Tools, blogs, and sources for automotive engineering. ![GitHub stars](https://img.shields.io/github/stars/ajay-bhojani/Awesome-Automotive?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/ajay-bhojani/Awesome-Automotive?style=flat)
- [Awesome-Automotive-Electronics](https://github.com/Leohc92/Awesome-Automotive-Electronics) - Automotive electronic systems knowledge and software. ![GitHub stars](https://img.shields.io/github/stars/Leohc92/Awesome-Automotive-Electronics?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Leohc92/Awesome-Automotive-Electronics?style=flat)
- [awesome-sdv](https://github.com/yzy-comfortuni/awesome-sdv) - Software-defined vehicle resources (AUTOSAR, Rust, DDS, SIL/HIL, OTA); Chinese / English. ![GitHub stars](https://img.shields.io/github/stars/yzy-comfortuni/awesome-sdv?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/yzy-comfortuni/awesome-sdv?style=flat)

**Security & vehicle buses**
- [awesome-vehicle-security](https://github.com/jaredthecoder/awesome-vehicle-security) - Vehicle security and car hacking. ![GitHub stars](https://img.shields.io/github/stars/jaredthecoder/awesome-vehicle-security?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/jaredthecoder/awesome-vehicle-security?style=flat)
- [awesome-canbus](https://github.com/iDoka/awesome-canbus) - CAN bus tools, hardware, and resources. ![GitHub stars](https://img.shields.io/github/stars/iDoka/awesome-canbus?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/iDoka/awesome-canbus?style=flat)
- [awesome-automotive-can-id](https://github.com/iDoka/awesome-automotive-can-id) - CAN IDs and payloads for various car models. ![GitHub stars](https://img.shields.io/github/stars/iDoka/awesome-automotive-can-id?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/iDoka/awesome-automotive-can-id?style=flat)
- [awesome-linbus](https://github.com/iDoka/awesome-linbus) - LIN bus tools and resources. ![GitHub stars](https://img.shields.io/github/stars/iDoka/awesome-linbus?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/iDoka/awesome-linbus?style=flat)
- [awesome-automotive-security](https://github.com/hexsecs/awesome-automotive-security) - Automotive security. ![GitHub stars](https://img.shields.io/github/stars/hexsecs/awesome-automotive-security?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/hexsecs/awesome-automotive-security?style=flat)
- [AwesomeSafetyAndSecurityForAuto](https://github.com/tengfeiwork/AwesomeSafetyAndSecurityForAuto) - Functional safety, SOTIF, and cybersecurity repositories. ![GitHub stars](https://img.shields.io/github/stars/tengfeiwork/AwesomeSafetyAndSecurityForAuto?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/tengfeiwork/AwesomeSafetyAndSecurityForAuto?style=flat)

**Autonomous driving & robotics**
- [awesome-robotic-tooling](https://github.com/Ly0n/awesome-robotic-tooling) - Tooling for robotics and autonomous driving (ROS, lidar, SLAM). ![GitHub stars](https://img.shields.io/github/stars/Ly0n/awesome-robotic-tooling?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/Ly0n/awesome-robotic-tooling?style=flat)
- [Awesome-Autonomous-Driving (autodriving-heart)](https://github.com/autodriving-heart/Awesome-Autonomous-Driving) - Autonomous driving resources. ![GitHub stars](https://img.shields.io/github/stars/autodriving-heart/Awesome-Autonomous-Driving?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/autodriving-heart/Awesome-Autonomous-Driving?style=flat)
- [Awesome-Autonomous-Driving (autonomousdrivingkr)](https://github.com/autonomousdrivingkr/Awesome-Autonomous-Driving) - Autonomous driving resources. ![GitHub stars](https://img.shields.io/github/stars/autonomousdrivingkr/Awesome-Autonomous-Driving?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/autonomousdrivingkr/Awesome-Autonomous-Driving?style=flat)
- [awesome-end-to-end-autonomous-driving](https://github.com/opendilab/awesome-end-to-end-autonomous-driving) - End-to-end autonomous driving. ![GitHub stars](https://img.shields.io/github/stars/opendilab/awesome-end-to-end-autonomous-driving?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/opendilab/awesome-end-to-end-autonomous-driving?style=flat)
- [awesome-vla-for-ad](https://github.com/worldbench/awesome-vla-for-ad) - Vision-language-action models for autonomous driving. ![GitHub stars](https://img.shields.io/github/stars/worldbench/awesome-vla-for-ad?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/worldbench/awesome-vla-for-ad?style=flat)

**EV**
- [awesome-ev-charging](https://github.com/juherr/awesome-ev-charging) - Tools for electric vehicle charging. ![GitHub stars](https://img.shields.io/github/stars/juherr/awesome-ev-charging?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/juherr/awesome-ev-charging?style=flat)

## Contributing

Pull requests welcome. Please:

1. Link to the official project page or repository (avoid blog mirrors).
2. Keep one line per entry: `[Name](URL) - Short description.` followed by badges when the entry is a GitHub repository (see the update rule below).
3. Prefer actively maintained projects; mark archived ones.
4. Keep entries alphabetical within a section where practical.

### Update Rule

Every entry that points to a GitHub repository carries [shields.io](https://shields.io) badges at the end of its line, in this order: stars, release date, last commit.

```markdown
![GitHub stars](https://img.shields.io/github/stars/OWNER/REPO?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-YYYY%2FMM%2FDD-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/OWNER/REPO?style=flat)
```

- Replace `OWNER/REPO` with the repository path. Stars and last-commit badges refresh automatically.
- **The release badge is static**: it shows the `published_at` date (UTC, YYYY/MM/DD) of the latest GitHub release and is rewritten at every refresh. If the repository has no published release, leave the release badge out and keep only stars and last commit.
- Entries added in the latest refresh carry a ![New](https://img.shields.io/badge/-NEW-red?style=flat) badge right after the entry name; it is removed at the next refresh.
- **shvyac's awesome lists** entries are the exception: link and stars badge only, no description.
- Use the repository root, not a subdirectory link. Entries that only link to a subdirectory of a repository listed elsewhere get no badges.
- Entries not hosted on GitHub (project sites, other dataset hosts, papers, forums), organization-only links, and the Commercial Reference section get no badges.
- When reviewing entries, check the last-commit badge. Mark or remove entries that look inactive or are archived.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-ai-dev-tools](https://github.com/shvyac/awesome-ai-dev-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-dev-tools?style=flat&label=%E2%AD%90)
- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-automotive-cae](https://github.com/shvyac/awesome-automotive-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-automotive-cae?style=flat&label=%E2%AD%90)
- [awesome-automotive-todo-mcp](https://github.com/shvyac/awesome-automotive-todo-mcp) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-automotive-todo-mcp?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-hpc](https://github.com/shvyac/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-mcp-ai](https://github.com/shvyac/awesome-mcp-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-mcp-ai?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-physical-ai-kaizen](https://github.com/shvyac/awesome-physical-ai-kaizen) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-physical-ai-kaizen?style=flat&label=%E2%AD%90)
- [awesome-quantum](https://github.com/shvyac/awesome-quantum) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-quantum?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
- [awesome-web-app-design](https://github.com/shvyac/awesome-web-app-design) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-web-app-design?style=flat&label=%E2%AD%90)
