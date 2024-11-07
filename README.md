# Reproduction of Recent CVEs

This repository is based on recently discovered CVEs and focuses on how to exploit, patch, and investigate the root causes of these vulnerabilities. DefHawk is working on high-critical CVEs that have caused significant damage to services, aiming to explore the extent of the impact.

Each section in this repository is dedicated to a specific vulnerability and contains all the information needed to set up a safe environment. Some sections also include instructions on exploiting the vulnerability in real-world scenarios. After thorough research, a detailed report will be attached to each section.

For a list of CVEs covered, see the following document:
[Google Sheets List of CVEs](https://docs.google.com/spreadsheets/d/1M6E_NRWxdLzWCeyMM0Dgepo36WiLItvFS30I3dHeWO0/)




# CVE-XXXX-XXXX


| **Step**                           | **Details**                                                                                                          | **Progress**      | 
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|-------------------|
| **Set up a Safe Testing Env**      |                                                                                                                      |   :heavy_check_mark:          |
| - Create a Virtual Lab             | Use VirtualBox, VMware, or Docker to create an isolated environment.                                                 |
|   - Choose a Suitable OS           | Install an OS compatible with the CVEs (e.g., Linux, Windows, or a specific version of software).                   |
|     - Install Necessary Tools      | Include tools like Metasploit, Burp Suite, or specific debugging tools relevant to the CVEs.                        |
| **Select Recent CVEs to Reproduce**|                                                                                                                      |
| - Severity and Exploitability      | Focus on CVEs with high CVSS scores and known exploitation in the wild.                                             |
|   - Availability of Public PoCs    | Choose vulnerabilities with available PoCs for easier reproduction.                                                  |
|     - Compatibility with My Env    | Ensure the CVE is compatible with your virtual lab setup (OS and software versions).                                |
| **Download and Set up the PoCs**   |                                                                                                                      |
| - Find the PoCs in Test Env        | Search on GitHub or Exploit-DB for reliable PoCs related to selected CVEs.                                           |
|   - Verify PoC and Audit           | Carefully read and test the PoC in a controlled environment; audit output to ensure it matches expected behavior.   |
| **Simulate and Document Process**  |                                                                                                                      |
| - Prepare Documentation            | Document each setup step, including OS, software versions, and configurations.                                       |
|   - Execute the Exploit            | Run the PoC and capture screenshots or logs to verify successful exploitation.                                       |
|     - Analyze the Results          | Explain how the vulnerability was exploited and why it works, with screenshots or logs as evidence.                |
| **Present the Findings**           |                                                                                                                      |
| - Overview of the CVEs             | Provide a brief summary, CVSS score, and affected software for each CVE.                                             |
|   - Reproduction Steps             | Include clear instructions for setting up and reproducing each CVE in a controlled environment.                      |
|     - Screenshots and Evidence     | Add screenshots or logs showing successful exploitation.                                                            |
|       - Mitigation                 | List any patches, configuration changes, or mitigations for each vulnerability.                                     |
| **Additional Tips**                |                                                                                                                      |
| - Security Practice and Approach   | Follow safe security practices and take a controlled "hacker" approach to prevent risks.                            |
