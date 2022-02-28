# OSFPGA Google Summer of Code 2022 - Project Ideas

The Open Source FPGA Foundation (OSFPGA) is applying as an umbrella organization for Google
Summer of Code (GSoC) 2022!

If OSFPGA is accepted into the program, open-source enthusiasts will have an opportunity to apply to
contribute to the democratization of FPGAs!

This page lists specific project proposals of interest to the OSFPGA community. Applicants would be
encouraged to propose ideas outside of this list, however project acceptance depends on our ability
to identify willing mentors. Mentors are available for the projects below.

See the [Google Summer of Code website](https://summerofcode.withgoogle.com/) for more information.
The roll of the "umbrella organization" is described
[here](https://google.github.io/gsocguides/mentor/org-application#a-note-on-umbrella-orgs).
More information about the application process will be provided if OSFPGA is accepted as an
umbrella organization.

## Project Ideas

### Hardware Object Technology (HOT)

HOT is a system that:

  - HOT class contains device independent methods and fields that deliver and use an FPGA
bitstream.
  - Takes an FPGA bitstream and turns it into a static array which can then be compiled into the
program or library.
  - Uses standard memory map driver and a portable DMA engine
  - Uses standard Linux read and write functions

_Skill level_: Advanced

Required skills:

  - FPGAs
  - Linux and Linux drivers
  - C++/Java

_Duration_: ~350 hours

_Mentor_: Steve Casselman


### Hotman

Hotman is a client/server architecture in which HOTs and commands can be issued to any node. It has a
plugin technology that allows easy integration of user routines. The user can create hardware objects by
reading in a bitstream and filling out information in a GUI.

_Skill level_: Advanced

_Required skills_:

  - FPGAs
  - Linux and Linux drivers
  - C++/Java
  - Scripting

_Duration_: ~350 hours

_Mentor_: Steve Casselman


### 1st CLaaS for Local FPGAs

[1st ClaaS](https://github.com/stevehoover/1st-CLaaS) supports web application communication with FPGA
logic in the cloud. It would be nice to support local FPGA use cases as well. This is useful for local
applications as well as to support development that will ultimately be deployed to the cloud.

[FuseSoC](https://github.com/olofk/fusesoc) and [Apio](https://github.com/FPGAwars/apio) are worth
considering for vendor-agnostic FPGA support.

_Discussion_: [TL-Verilog User's Slack workspace](https://join.slack.com/t/tl-verilog-users/shared_invite/zt-4fatipnr-dmDgkbzrCe0ZRLOOVm89gA) `#1st-claas` channel.

_Skill level_: Advanced

_Required skills_:
  - FPGAs
  - Linux
  - Scripting
  - Makefiles

_Duration_: ~350 hours

_Mentor_: [Theo Omtzigt](https://www.linkedin.com/in/theodoreomtzigt/) ([email](mailto:theo@stillwater-sc.com)), [Steve Hoover](https://www.linkedin.com/in/steve-hoover-a44b607/) ([email](mailto:steve.hoover@redwoodeda.com))


## World CLaaS: Open FPGA Cloud

The vision is to enable individuals with FPGAs (World CLaaS Citizens) to share their hardware with the world.
The system would include three (open-source) parts:

  - Citizens (of the World): An FPGA resource contributed to the World (not a person).
  - World: A registry of World Citizens available for Jobs/Missions. Interest (permission) is based
    on tokens (that can be provided to certain Causes, users, etc.).
  - Mission/Job API: API for a Citizen to perform a task for a Cause (aka the API to run an FPGA accelerator).

Vendor software licenses restrict the use model, so initial development will focus on open-source FPGA tools.
Some notes on hosting FPGAs can be found
[here](https://medium.com/@shariethernet/quick-remote-fpga-lab-setup-without-vpn-port-forwarding-firewall-configurations-and-other-ccd45489ab35).
Specifically, this summer project will be to develop the initial Worldwide Registry. Citizens will be registered
via an API. Missions will be assigned via an API. A web front-end will present the state of the World.

_Skill level_: Advanced

_Required skills_
  - Web development
  - Databases

_Duration_: ~350 hours

_Mentor_: [Steve Hoover](https://www.linkedin.com/in/steve-hoover-a44b607/) ([email](mailto:steve.hoover@redwoodeda.com))
  Secondary: [Kunal Ghosh](https://www.linkedin.com/in/kunal-ghosh-vlsisystemdesign-com-28084836/) ([email](mailto:kunalpghosh@gmail.com))


### Virtual FPGA Lab

![virtual lab](https://user-images.githubusercontent.com/64545984/130665673-63e52c11-f5e4-4290-8d05-a5a0741fbbbd.png)

This project provides on online virtual lab that mimics the physical lab experience. It offers

  - the FPGA experience for folks who do not have access to FPGAs
  - a light-weight online development environment for FPGA logic
  - an extension of physical lab classes outside of the physical lab

This project began as a Google Summer of Code 2021 project under the Free and Open Source Silicon Foundation [here](https://github.com/BalaDhinesh/Virtual-FPGA-Lab).
It was written up in this [blog](https://medium.com/@m.baladhinesh/fpgas-in-your-browser-bb92be1c1fa3).
[Course content](https://github.com/stevehoover/GettingStartedWithFPGAs) based on the lab is in development.

Possible enhancements:

  - support for additional FPGA boards and peripherals
  - starting templates providing FPGA shell logic for various platforms
  - course content
  - an integration with [FuseSoC](https://github.com/olofk/fusesoc) and/or [Apio](https://github.com/FPGAwars/apio)
    for a vendor-agnostic build flow

_Difficulty Level_: Intermediate

_Required skills_:

  - FPGAs
  - JavaScript and Makerchip.com Visual Debug feature
  - TL-Verilog

_Discussion_: [TL-Verilog User's Slack workspace](https://join.slack.com/t/tl-verilog-users/shared_invite/zt-4fatipnr-dmDgkbzrCe0ZRLOOVm89gA) `#virtual-fpga-lab` channel.

_Duration_: ~175 hours

_Mentor_: [Steve Hoover](https://www.linkedin.com/in/steve-hoover-a44b607/) ([email](mailto:steve.hoover@redwoodeda.com))


### Development Framework for Open MPW Shuttles

Efabless, Google, and SkyWater Technologies, through the Open MPW and ChipIgnite programs, provide free ASIC fabrication.
To help streamline the development flow, this project will provide a starting template for development within the
free online Makerchip IDE. This will include:

  - visualization of the [Caravel](https://github.com/efabless/caravel) harness
  - support for FPGA prototyping, leveraging this [environment](https://github.com/BalaDhinesh/Virtual-FPGA-Lab)
  - default stimulus
  - build flow enhancements to the [Caravel sample user project](https://github.com/efabless/caravel_user_project),
    adding support for TL-Verilog and Makerchip
  - clear development flow documentation

_Difficulty Level_: Intermediate/Advanced

_Required skills_

  - Open MPW/ChipIgnite
  - OpenLane
  - FPGAs
  - TL-Verilog
  - Makerchip
  - Documentation

_Duration_: ~175 or ~350 hours

_Mentor_: one of several Efabless guys, ([email](mailto:tim@opencircuitdesign.com)), Secondary: [Steve Hoover](https://www.linkedin.com/in/steve-hoover-a44b607/) ([email](mailto:steve.hoover@redwoodeda.com))


### FractalValley

![fractalvalley](https://user-images.githubusercontent.com/11302288/134257481-e43618a9-a3de-4623-9c6d-75a1b009c076.png)

OSFPGA believes passionately in the potential of FPGAs to accelerate cloud computing and web applications.
[FractalValley.net](http://fractalvalley.net) showcases this FPGA use model.

This project will focus on enhancing the user experience of [FractalValley.net](http://fractalvalley.net) to more strongly convey to the community the
potential of hardware-accelerated web applications.

_Skill Level_: Intermediate

_Required skills_:

  - Web development (JavaScript, HTML, CSS, React, NodeJS, etc.)
  - UI/UX

_Duration_: ~175 or ~350 hours

_Mentor_: [Flyyn Leonard](https://www.linkedin.com/in/codelenny/), Secondary: [Steve Hoover](https://www.linkedin.com/in/steve-hoover-a44b607/)


### Neural Network on FPGA

Like [warp-v.org](https://warp-v.org) demonstrates configurable, visualizable CPU cores that can be run on FPGA, this project will contribute to similar configurable, visualizable, neural network logic. A simple example is provided by the mentor at: https://github.com/vineetjain07/DNN_TL-V. This project will use the free Makerchip.com IDE, and the model will be coded in TL-Verilog.

This project is multi-facited. Contributors will focus on multiple, but not all of the following aspects of the project. Applications should clearly define a realistic scope and timeline that target the applicant's strengths.

  - TL-Verilog logic, configurable using M4.
  - Visualization of the logic using Makerchip's Visual Debug feature.
  - FPGA implementation of the logic using this [Virtual FPGA Lab](https://github.com/os-fpga/Virtual-FPGA-Lab) and exporting to and testing on physical FPGAs.
  - Web front-end configurator for the ML logic.

The resulting work will be useful in an educational context to demonstrate neural networks, digital logic design, and transaction-level design methodology.

_Skill level_: Advanced

_Required skills_:

  - TL-Verilog
  - Macro preprocessing
  - Makerchip
  - FPGAs
  - Web development, including React

_Duration_: ~350 hours

_Mentor_: [Vineet Jain](https://www.linkedin.com/in/vineetjain78/), Secondary: [Steve Hoover](https://www.linkedin.com/in/steve-hoover-a44b607/)


## WIP proposals

1st CLaaS or FireSim Port to VMAccel

Duration: ~350 hours

