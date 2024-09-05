# Risk Summary

Risks provide insights into the security health of your applications. Risks are identified as:

* **Malicious Packages**: Malicious packages are Runtime objects identified as containing harmful or malicious code, posing a threat to your system by executing unauthorized actions. Runtime is designed to detect and flag these packages, effectively preventing potential security breaches.
* **Untrusted Images**: Untrusted images are sourced from registries that lack recognition or verification of trustworthiness. Utilizing such images can introduce security risks. Runtime identifies and alerts users against the use of untrusted images in the Runtime environment, promoting the use of only reliable sources.
* **Critical  and Applicable CVEs**: Critical and Applicable CVEs (Common Vulnerabilities and Exposures) are vulnerabilities classified as critical in severity and determined to be applicable through Contextual Analysis  part of JFrog Advanced Security.&#x20;
* **Integrity Violation**: Integrity violations occur when the checksum of the Runtime image differs from the checksum of the originally deployed image from Artifactory. This disparity may indicate image tampering or corruption. Runtime ensures the integrity of Runtime objects by consistently comparing checksums.

<figure><img src="../.gitbook/assets/Screenshot 2024-09-03 at 16.11.10.png" alt=""><figcaption></figcaption></figure>
