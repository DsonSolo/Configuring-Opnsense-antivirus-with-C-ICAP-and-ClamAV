**Configuring Opnsense antivirus with C-ICAP and ClamAV**

In this lab, I successfully configured Opnsense antivirus by integrating
C-ICAP and ClamAV, ensuring a robust defense against potential threats.

**REQUIREMENTS:**

- Establishment of a Multi-LAN Virtual Environment from Lab 3.0

- Availability of 2 Windows 10 client PCs

- Opnsense Firewall configured with 2 LAN interfaces

**Note:** The c-icap and ClamAV plugins are pre-installed on OPNsense
for seamless integration.

**STEPS:**

**Configuring C-ICAP and ClamAV:**

Navigate to Services \> C-ICAP \> Configuration

Implement necessary configurations to enhance the effectiveness of the
antivirus setup.

<img src="./media/image1.png" style="width:5.69271in;height:3.6218in" />

Before proceeding with the steps, it's crucial to take a snapshot of all
machines to ensure a safe starting point.

**Step 1: Configure C-ICAP and ClamAV.**

Continuing our meticulous journey through the Opnsense Antivirus lab,
the next crucial step was to activate the c-icap service, with a focus
on default settings. It's worth noting that the comprehensive help
feature was enabled to grasp the intricacies of each configuration.

**Operational Steps:**

1.  **Activating c-icap Service:**

- Navigated to the Services section, specifically the C-ICAP
  Configuration.

- Enabled the c-icap service, leaving all other configurations at their
  default settings.

<img src="./media/image2.png"
style="width:5.20313in;height:2.61072in" />

**Note:** The full help feature played a pivotal role in gaining a
comprehensive understanding of the various settings.

2.  **Empowering ClamAV:**

- Moved on to the Antivirus tab to initiate the enabling of ClamAV.

- Opted for default configurations for our demonstration.

- Executed the crucial save command to implement the changes.

> <img src="./media/image3.png" style="width:6.5in;height:1.43056in" />

3.  **ClamAV Signature Download:**

- Extended the configuration journey to Services \> ClamAV \>
  Configuration.

- Initiated the download of signatures, with a keen eye on the detailed
  setting descriptions.

> <img src="./media/image4.png"
> style="width:6.13021in;height:2.76056in" />

While awaiting the download, the full help feature remained enabled,
ensuring a thorough comprehension of the settings.

This meticulous approach ensures a robust antivirus setup, ready to
shield our network against potential threats.

Continuing the journey to reinforce Opnsense's antivirus defenses, I
proceeded to activate the clamd and freshclam services. Below is a
detailed account of the steps taken to further bolster my defense
system.

**Operational Steps:**

**1. Activating ClamAV Services:**

- Embarked on the first operational stride by enabling both clamd and
  freshclam services. Throughout this process, I adhered to default
  settings for other configurations.

> <img src="./media/image5.png" style="width:6.34167in;height:4.2in" />

- To cement these changes, I executed the save command, fortifying the
  foundation of my antivirus setup.

<img src="./media/image6.png" style="width:6.5in;height:1.16667in" />

**2. Dashboard Verification:**

- Transitioned to the dashboard to meticulously verify the activation
  status of Clamd (ClamAV Daemon). This validation step ensures that the
  critical antivirus components are actively engaged in safeguarding the
  system.

<img src="./media/image7.png" style="width:6.5in;height:2.05556in" />

**3. ICAP Integration:**

- I explored the Web Proxy settings by going through the options at Web
  Proxy \> Administration \> Forward Proxy options \> ICAP settings.

> <img src="./media/image8.png" style="width:6.5in;height:3.08333in" />

- Enabled ICAP, a strategic move pivotal for elevating the robustness of
  the antivirus infrastructure.

- I applied the changes meticulously, ensuring seamless integration of
  ICAP into the overall system.

<img src="./media/image9.png" style="width:6.5in;height:3.70833in" />

**Step 2: Testing Antivirus**

I navigated to Guest PC2, ensuring a snapshot was taken to secure my
system. It was crucial as misconfigurations in ClamAV might expose the
system to potential virus downloads.

I conducted a Google search for the eicar test and clicked on the first
link.

<img src="./media/image10.png" style="width:6.5in;height:3.52778in" />

Upon clicking various links, Windows Defender intervened, demonstrating
its protective function. I deliberately chose to proceed to simulate
scenarios where Windows Defender might fail.

<img src="./media/image11.png"
style="width:6.23958in;height:2.15625in" />

The successful blocking of the site confirmed the effectiveness of the
Opnsense ClamAV configuration in safeguarding the system.

<img src="./media/image12.png" style="width:6.5in;height:5.22222in" />

**Step 3: Reviewing Log Files**

I accessed the log files through Services \> C-ICAP-Log File.

<img src="./media/image13.png" style="width:6.5in;height:3.09722in" />

The logs provided a comprehensive overview of antivirus activities,
indicating successful detections.

<img src="./media/image14.png" style="width:6.5in;height:2.47222in" />

With this, the lab concluded, showcasing the practicality and efficacy
of the implemented antivirus measures.
