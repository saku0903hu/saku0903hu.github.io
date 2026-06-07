
**Course:** VLSI Technology I  
**Title:** VLSI Technology I Final Report  
**Author:** Takeru SAKAI  
**Date:** June 7, 2026  

---

## (1) Pros and Cons of Specific Key Technologies in the Joined Group (10nm FinFET)

This section focuses on the introduction of Cobalt (Co) interconnects and the associated process integration challenges in the Intel 10nm FinFET process node.

### Pros (Advantages)
* **Transition to Cobalt Interconnects:** In the Intel 10nm process, the interconnect material for the lowest metal layers (M0 and M1) transitions from conventional copper to Cobalt (Co), utilizing a Titanium Nitride (TiN) liner.
* **Enhanced Interconnect Reliability:** The primary advantage of adopting cobalt lies in its significantly enhanced electromigration resistance. This directly addresses the critical issue of reliability degradation in interconnects caused by aggressive scaling, while successfully enabling a thinner liner design.
* **Structural Innovations:** For the M0 and M1 layers, a technique that physically embeds different materials to interrupt the wiring is implemented to optimize routing. Furthermore, a new spacer scheme that completely seals off the bottom of the Shallow Trench Isolation (STI) is introduced, successfully balancing advanced downsizing with overall structural stability.

### Cons (Disadvantages)
* **Extreme Process Integration Complexity:** The introduction of these novel materials and structures drastically increases the difficulty of process integration, leading to very tight process margins.
* **Lithography Limitations and VC Spikes:** During Via Contact Trench (VCT) formation, shrinking via lithography through conventional shrink spacers is unfeasible, making the process heavily reliant on material selectivity. Due to the low selectivity of the materials, "VC spikes"—the same defect that caused initial yield issues in the 14nm generation—still occur.
* **Severe Structural Defects and Yield Loss:** Significant epitaxial layer erosion is observed in the Single Diffusion Break (SDB) regions, and substantial variation remains in the gate profiles. These accumulated process variations lead to tight margins and present a major challenge in terms of manufacturing yield degradation.

---

## (2) Pros and Cons of Specific Key Technologies in the Non-Joined Group (14nm SoC)

Based on the technical data regarding the Intel 14nm Tri-Gate FinFET SoC (Cherry Trail Z8700), this section analyzes the W fill (Tungsten fill) and High-k/Metal Gate (HKMG) materials utilized in the transistor gate stack.

### Pros (Advantages)
* **Excellent Electrical and Thermal Characteristics:** Tungsten fill (W fill) is adopted to fill the internal gate structure and provide electrical conduction. Because of its low resistance and superior thermal stability, it contributes significantly to enhancing transistor performance.
* **High Nanoscale Energy Efficiency:** By combining Hafnium Oxide (HfO$_2$) as a High-k gate dielectric to reduce leakage current with Titanium Aluminum Carbide (TiAlC) to optimize threshold voltage, high energy efficiency and performance are achieved at the nanoscale.
* **Enhanced Reliability through Layer Optimization:** Thickening metal layers such as tungsten and copper improves structural reliability, voltage tolerance, and overall electrical conduction.

### Cons (Disadvantages)
* **Escalating Manufacturing Costs and Complexity:** Utilizing these high-performance materials complicates the fabrication process and escalates costs. For instance, the deposition of TiAlC requires a highly controlled, sophisticated process.
* **Difficult Dimension Control:** As scaling progresses, Critical Dimension (CD) control becomes increasingly difficult. When fabrication accuracy declines, severe structural defects arise, such as missing fins or high resistance caused by insufficient metal gate wrap-around.
* **Device Performance Degradation:** These process variations ultimately trigger increases in leakage current, threshold voltage fluctuations, and reduced drive strength, leading to a decline in both device reliability and overall manufacturing yield.

---

## (3) Desired New Functions and Characteristics for Smartphones and Future Electronic Devices

### Desired New Functions and Characteristics
The ultimate capability I desire for future electronic devices, such as smartphones, is the complete harmonization of **"ultimate ultra-low power consumption requiring no charging for several weeks"** and **"advanced edge AI processing capabilities capable of executing complex models locally on the device without relying on cloud servers."** In current devices, a severe trade-off exists where demanding high computational power results in rapid and unsustainable battery drain.

### Required Technological Elements
To overcome this trade-off, conventional process limitations must be broken through. Specifically, it is necessary to resolve the technical bottlenecks observed in current architectures, such as gate profile variations in FinFETs, tight process margins that lower yield, and increased leakage current caused by the degradation of CD control. 

The following technological elements are indispensable to achieve this goal:
* **GAA (Gate-All-Around) Transistor Architecture:** Transitioning from FinFETs to next-generation GAA structures. By wrapping the gate around the channel from all four sides, gate controllability is maximized to its absolute limit, drastically suppressing leakage current.
* **Advanced Novel Interconnect Materials:** Further developing and optimizing new interconnect material technologies, such as Cobalt (Co), to dramatically enhance electromigration resistance under extreme scaling and ensure reliable high-speed data paths.

### My Actions
To help realize these next-generation technologies, I will deepen my expertise in semiconductor device engineering and materials science. 

Specifically, I intend to take the following actions:
1. **Research on Next-Generation Deposition Processes:** To suppress epitaxial layer erosion and dimension variations to the absolute minimum, I will focus on next-generation deposition processes such as ALD (Atomic Layer Deposition), which can precisely control film thickness and uniformity at the atomic level.
2. **Bridging Design and Manufacturing:** I will practically master robust circuit design methodologies that natively assume and tolerate process variations. By doing so, I aim to contribute to next-generation LSI development projects as an engineer who can bridge the gap between manufacturing yield challenges and circuit design, driving the future of semiconductor innovation.