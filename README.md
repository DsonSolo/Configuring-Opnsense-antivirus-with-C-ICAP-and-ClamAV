*Configuring Opnsense antivirus with C-ICAP and ClamAV*

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

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image1.png)

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

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image2.png)

**Note:** The full help feature played a pivotal role in gaining a
comprehensive understanding of the various settings.

2.  **Empowering ClamAV:**

- Moved on to the Antivirus tab to initiate the enabling of ClamAV.

- Opted for default configurations for our demonstration.

- Executed the crucial save command to implement the changes.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image3.png)

3.  **ClamAV Signature Download:**

- Extended the configuration journey to Services \> ClamAV \>
  Configuration.

- Initiated the download of signatures, with a keen eye on the detailed
  setting descriptions.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image4.png)

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

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image5.png)

- To cement these changes, I executed the save command, fortifying the
  foundation of my antivirus setup.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image6.png)

**2. Dashboard Verification:**

- Transitioned to the dashboard to meticulously verify the activation
  status of Clamd (ClamAV Daemon). This validation step ensures that the
  critical antivirus components are actively engaged in safeguarding the
  system.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image7.png)

**3. ICAP Integration:**

- I explored the Web Proxy settings by going through the options at Web
  Proxy \> Administration \> Forward Proxy options \> ICAP settings.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image8.png)

- Enabled ICAP, a strategic move pivotal for elevating the robustness of
  the antivirus infrastructure.

- I applied the changes meticulously, ensuring seamless integration of
  ICAP into the overall system.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image9.png)

**Step 2: Testing Antivirus**

I navigated to Guest PC2, ensuring a snapshot was taken to secure my
system. It was crucial as misconfigurations in ClamAV might expose the
system to potential virus downloads.

I conducted a Google search for the eicar test and clicked on the first
link.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image10.png)

Upon clicking various links, Windows Defender intervened, demonstrating
its protective function. I deliberately chose to proceed to simulate
scenarios where Windows Defender might fail.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image11.png)

The successful blocking of the site confirmed the effectiveness of the
Opnsense ClamAV configuration in safeguarding the system.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image12.png)

**Step 3: Reviewing Log Files**

I accessed the log files through Services \> C-ICAP-Log File.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image13.png)

The logs provided a comprehensive overview of antivirus activities,
indicating successful detections.

![Screenshot](https://github.com/DsonSolo/Configuring-Opnsense-antivirus-with-C-ICAP-and-ClamAV/blob/main/image14.png)

With this, the lab concluded, showcasing the practicality and efficacy
of the implemented antivirus measures.
