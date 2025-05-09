# OpenSOC

### Initial Setup

**Oracle VirtualBox**
![vmbox](day1/vmbox.png)

**VM Desktop View**
![vm](day1/vm.png)

---

## Day 1: Sky130 – Inception of open-source EDA, OpenLANE and Sky130 PDK

<details>
  <summary> <strong>SKY130_D1_SK1 - How to talk to computers</strong></summary>

<br>

* ![sky\_11\_l1](day1/sky_11_l1.png)
* ![sky\_11\_l2](day1/sky_11_l2.png)
* ![sky\_11\_l3](day1/sky_11_l3.png)

</details>

<details>
  <summary> <strong>SKY130_D1_SK2 - SoC design and OpenLANE</strong></summary>

<br>

* ![sky\_12\_l1](day1/sky_12_l1.png)
* ![sky\_12\_l2](day1/sky_12_l2.png)
* ![sky\_12\_l3](day1/sky_12_l3.png)
* ![sky\_12\_l4](day1/sky_12_l4.png)

</details>

---

### ⚙️ SKY130\_D1\_SK3 - Get familiar with open-source EDA tools

This part focuses on understanding the EDA environment and flow using the OpenLANE toolchain on the Sky130 PDK.

**🔹 Directory Structure**
Initial directory structure and setup for OpenLANE workspace:

![file\_struc](day1/file_struc.png)

---

**🔹 Launching OpenLANE (Docker)**
Start by entering the OpenLANE working directory and launching the tool in interactive mode using Docker:

```bash
cd Desktop/work/tools/openlane_working_dir/openlane/
docker
flow.tcl -interactive
```

This will initialize the OpenLANE environment.

![openlane\_start](day1/openlane_start.png)

---

**🔹 Preparing the Design: `picorv32a`**

Run the preparation step for the `picorv32a` design using:

```tcl
prep -design picorv32a
```

This sets up the flow and generates initial logs and configuration files.

![prep](day1/prep.png)
![files\_after\_prep](day1/files_after_prep.png)
![config\_tcl](day1/config_tcl.png)

---

**🔹 Running Synthesis**

Once the prep is complete, proceed with synthesis using:

```tcl
run_synthesis
```

This runs the synthesis step with Yosys, generating a report of the synthesized design.

* Terminal output after synthesis:
  ![after\_run\_synth](day1/after_run_synth.png)

* Flop ratio and statistics (e.g., DFF, total cells):
  ![flop\_ratio](day1/flop_ratio.png)

* Yosys synthesis stats report:
  ![synth\_stats\_report](day1/synth_stats_report.png)

