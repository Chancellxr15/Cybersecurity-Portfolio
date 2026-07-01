# Final Risk Mitigation Plan — Health Network

***FINAL RISK MITIGATION PLAN***

**By: Chance Debbs**

**Risk Management Plan *-- Health Network***

**1. Introduction**

The purpose of this Risk Management Plan is to create a structured process for identifying, analyzing, and responding to risks that threaten the confidentiality, integrity, and availability of Health Network's assets. Risk management is essential for protecting sensitive health information, sustaining customer trust, meeting compliance obligations, and ensuring the delivery of healthcare services. As Health Network operates in a highly regulated and mission-critical environment, risk management supports the company's goals of providing secure electronic medical messaging, and payment processing. This plan will serve as a living document, updated regularly to address new and emerging threats, changes in compliance regulations, and evolving technologies.

**2. Scope and Boundaries**

-   **Products**: HNetExchange, HNetPay, HNetConnect.

-   **Infrastructure**: Three production data centers hosting around 1,000 servers, vendor dependency locations, corporate IT systems, and employee-issued laptops and mobile devices.

-   **Employees**: Around 600 staff members, including corporate, IT, security, and operations teams.

-   **Locations**: Headquarters in Minneapolis, Minnesota, with other offices in Portland, Oregon, and Arlington, Virginia.

-   **Threats**: Internal and external threats, natural disasters, hardware loss, insider threats, regulatory changes, and digital attacks.

-   Boundaries strictly include only Health Network-owned infrastructure and operations.

**3. Applicable Laws and Regulations**

-   **Health Insurance Portability and Accountability Act**: Protects patient health information and enforces administrative, technical, and physical safeguards.

-   **Health Information Technology for Economic and Clinical Health Act**: Expand HIPAA by addressing breach notification and electronic health records.

-   **Payment Card Industry Data Security Standard**: Required for HNetPay operations to secure credit card transactions.

-   **Federal Trade Commission Safeguards Rule**: Governs the protection of consumer financial data.

-   **General Data Protection Regulation For European patients**: Governs privacy and security of personal data for European citizens.

-   **State Privacy Laws**: Require specific security and privacy protections for residents' data.

**Failure to comply with these regulations may result in penalties, reputational harm, or loss of business. **

**4. Roles and Responsibilities**

-   **Chief Information Security Officer (CISO):** Oversees risk management strategy, ensures regulatory compliance, and reports to executive leadership.

-   **IT Security Team:** Conducts risk assessments, implements controls, manages incident response, and maintains security monitoring.

-   **IT Operations Team:** Manages production systems, change management, and ensures availability of services.

-   **Compliance Officer:** Ensures adherence to HIPAA, HITECH, PCI DSS, and state requirements.

-   **Department Managers:** Identify and communicate risks within their business units.

-   **Employees:** Follow security policies, report incidents, and safeguard company assets.

-   **Senior Management:** Provides funding, strategic direction, and support for risk management initiatives.

**5. Proposed Schedule**

-   **Week 1--2:** Begin project, assign roles, gather existing documentation, and define risk categories.

-   **Week 3--4:** Conduct risk assessments, identify threats, and document vulnerabilities.

-   **Week 5--6:** Perform a qualitative risk analysis, assign likelihood and impact values, and prioritize risks.

-   **Week 7--8:** Develop risk mitigation strategies and assign responsibilities.

-   **Week 9:** Review compliance requirements, finalize risk register, and prepare draft plan.

-   **Week 10:** Present plan to senior management, gather feedback, and finalize the document.

-   **Ongoing:** Quarterly reviews and annual updates to for new threats and regulatory changes.

**6. Draft Risk Management Plan Outline**

1.  **Introduction**

    -   Purpose and importance

    -   Risk management objectives

2.  **Scope and Boundaries**

    -   Systems, products, people, and locations covered

    -   Boundaries and exclusions

3.  **Regulatory Compliance Requirements**

    -   HIPAA, HITECH, PCI DSS, GDPR, and state privacy laws

4.  **Risk Management Methodology**

    -   Risk identification

    -   Qualitative risk assessment

    -   Mitigation strategies

    -   Monitoring and review

5.  **Roles and Responsibilities**

    -   CISO, IT Security, IT Operations, Compliance, Management, Employees

6.  **Risk Assessment Schedule**

    -   Timeline and milestones

    -   Ongoing updates and reviews

7.  **Reporting and Communication**

    -   Risk register and dashboard updates

    -   Management reporting processes

8.  **Plan Maintenance**

    -   Annual reviews

    -   Trigger-based updates (new regulations, technology changes, incidents)

***Risk Assessment Plan -- Health Network***

**Introduction**

The purpose of this Risk Assessment Plan is to guide Health Network in identifying, analyzing, and prioritizing risks to its operations, assets, and data. As a healthcare organization handling sensitive patient and financial information, Health Network faces exposure to cyberattacks, data breaches, insider misuse, and regulatory penalties. This approach allows management to make decisions about resource use and mitigation strategies.

**Scope and Boundaries**

-   **Data Centers**: Minneapolis, Portland, and Arlington production facilities.

-   **Products**: HNetExchange, HNetPay, and HNetConnect.

-   **Corporate Assets**: 1,000 production servers, 650 corporate laptops, and mobile devices.

-   **Third-Party Integrations**: Payment processors, co-location hosting vendors.

-   **Networks and Internet-Facing Systems**: HTTPS connections, firewalls, VPNs.

-   **Exclusions**: personally owned employee devices, non-production test environments.

**Assets and Activities to Be Assessed**

-   **Applications**:

    -   *HNetExchange*: secure messaging service for hospitals.

    -   *HNetPay*: payment portal interacting with credit card processors.

    -   *HNetConnect*: online medical directory with doctor profiles.

-   **Infrastructure**: Data center servers, storage, networking equipment.

-   **Corporate Devices**: Laptops and mobile devices with PHI/PII access.

-   **Data**: Electronic medical records (EMR), billing records, PII/PHI.

-   **Operations**: Patch/change management, disaster recovery, vendor SLAs.

**Threats and Vulnerabilities**

**Threats**

-   Data theft from stolen or removed hardware.

-   Loss of data from stolen or lost laptops and mobile devices.

-   Production outages (natural disasters, software instability, change failures).

-   Internet threats (DDoS, ransomware, SQL injection, phishing).

-   Insider threats (malicious or accidental).

-   Regulatory risks (HIPAA, PCI DSS, HITECH).

-   Supply chain risks.

-   Credential theft through social engineering.

**Vulnerabilities**

-   Gaps in encryption and access controls.

-   Weak endpoint monitoring.

-   Disaster recovery plans not fully tested.

-   Lack of employee training on phishing and social engineering attacks.

-   Limited monitoring of insider activity.

**Controls to Be Assessed**

-   **Preventive**: MFA, encryption, firewalls, least-privilege access.

-   **Detective**: SIEM logging, IDS/IPS, vulnerability scanning.

-   **Corrective**: Incident response, system backup/recovery, patch management.

-   **Administrative**: Policies, vendor compliance, employee training, change control.

**Roles and Responsibilities**

-   **Senior Management**: Approve assessment scope, allocate funding, accept residual risk.

-   **CISO**: Lead the assessment, ensure regulatory compliance.

-   **IT Security Team**: Conduct scans, penetration testing, log monitoring.

-   **Data Center Ops**: Maintain physical and infrastructure security.

-   **Business Unit Leaders**: Identify critical processes, provide input on risk tolerance.

-   **Employees**: Comply with security policy, complete training, report suspicious activity.

-   **Vendors**: Uphold SLA requirements, maintain compliance certifications.

**Risk Assessment Approach (Qualitative)**

This risk assessment will categorize risk by Likelihood (Low/Medium/High) and Impact (Low/Medium/High). Risks are rated in a matrix, having a final level as Critical, High, Medium, or Low.

**Matrix:**

  ---------------------------------------------------------------------------------
  **Threat**                  **Likelihood**    **Impact**        **Risk Level**
  --------------------------- ----------------- ----------------- -----------------
  Data center outage          **Medium**        **High**          **High**

  Stolen laptop with PHI      **High**          **High**          **Critical**

  Insider misuse              **Low**           **High**          **Medium**

  Regulatory non-compliance   **Medium**        **High**          **High**
  ---------------------------------------------------------------------------------

**Schedule**

  -------------------------------------------------------------------------------------------
  **Phase**         **Activity**                      **Timeline**      **Responsible**
  ----------------- --------------------------------- ----------------- ---------------------
  **Phase 1**       Planning & Scoping                Weeks 1--2        IT Security

  **Phase 2**       Asset Identification              Weeks 2--3        IT, Business Units

  **Phase 3**       Threat & Vulnerability Analysis   Weeks 3--5        IT Security

  **Phase 4**       Control Review                    Weeks 5--6        Security & Data Ops

  **Phase 5**       Risk Evaluation                   Weeks 6--7        IT Security, Mgmt.

  **Phase 6**       Report & Recommendations          Weeks 8--9        CISO, Mgmt.

  **Phase 7**       Review & Approval                 Week 10           Senior Mgmt.
  -------------------------------------------------------------------------------------------

**Risk assessments will be updated annually, or after a major incident or regulatory changes.**

**Conclusion**

This plan provides Health Network with a structured framework to identify risks, assess potential impacts, and prioritize mitigation strategies. This assessment defines standards to make sure the plan follows industry best practices, while qualitative methods allow for prioritization of risks.

**Risk Mitigation Plan - Health Network, Inc.**

**1. Introduction**

This Risk Mitigation Plan is designed to address threats identified during the company's risk assessment. The plan prioritizes the protection of patient data, continuity of service, compliance with healthcare and payment regulations, and reduction of financial and reputational impact from potential incidents.

**2. Purpose and Objectives**

The purpose of this Risk Mitigation Plan is to establish strategies and controls to reduce the probability and impact of risks that threaten Health Network's information assets. The specific objectives are to:

-   Minimize exposure to data breaches, data loss, and service disruptions.

-   Ensure compliance with HIPAA, PCI-DSS, and state data protection laws.

-   Enhance system resilience, employee awareness, and incident response capabilities.

-   Support business continuity and disaster recovery operations across all three corporate locations and data centers.

**3. Summary of Identified Threats**

  -------------------------------------------------------------------------------------------------------------------------------------
  **Threat Description**                                                          **Potential Impact**
  ------------------------------------------------------------------------------- -----------------------------------------------------
  Loss of company data due to hardware removal or theft from production systems   Loss of PHI and intellectual property

  Loss of data due to stolen/lost laptops or mobile devices                       Unauthorized disclosure of sensitive information

  Production outages (natural disasters, unstable software, or failed changes)    Downtime, customer loss, financial loss

  Internet threats (malware, DDoS)                                                Data breaches, denial of service, reputation damage

  Insider threats (malicious or negligent employees)                              Data theft, sabotage, or compliance violations

  Regulatory changes impacting compliance                                         Noncompliance fines, operational changes

  Emerging threats (cloud vulnerabilities, phishing, ransomware)                  Credential theft, service disruption
  -------------------------------------------------------------------------------------------------------------------------------------

**4. Risk Mitigation Strategies**

**Data Protection and Access Controls**

-   **Encryption:**\
    Implement full-disk encryption such as BitLocker on all laptops and mobile devices. Encrypt all sensitive data at rest and in transit using AES-256.

-   **Access Management:**\
    Deploy Role-Based Access Control and Least Privilege principles across all systems. Integrate MFA for VPN, web portals, and administrative access.

-   **Data Loss Prevention (DLP):**\
    Install DLP tools on endpoints and mail gateways to detect and block exfiltration of sensitive data.

-   **Asset Tracking:**\
    Utilize Mobile Device Management software to remotely wipe or disable lost/stolen devices. Require regular check-ins for all assets.

**Physical and Environmental Security**

-   **Data Center Controls:**\
    Partner with data center vendors to ensure 24/7 surveillance, biometric access, and hardware tamper detection.

-   **Asset Tagging:**\
    Tag all production hardware and conduct quarterly audits to ensure no unauthorized hardware removal.

-   **Environmental Safeguards:**\
    Install fire suppression, uninterruptible power supplies, and redundant cooling systems to maintain up time.

**Network and System Security**

-   **Firewall and IDS/IPS:**\
    Configure NGFW and IDS/IPS at each data center. Implement Splunk or another SIEM, or Suricata for real-time alerting and log analysis.

-   **Web Application Security:**\
    Perform quarterly vulnerability scans and annual penetration tests of HNetExchange, HNetPay, and HNetConnect web servers. Enable WAF to block SQL injections, XSS, and DDoS attempts.

-   **Patch Management:**\
    Automate OS and software patching using centralized tools. Critical patches must be deployed within 48 hours of release.

-   **Network Segmentation:**\
    Separate production, development, and administrative networks. Implement VLANs and zero-trust principles to restrict lateral movement.

**Business Continuity and Disaster Recovery**

-   **Data Backups:**\
    Perform daily incremental and weekly full backups to both on-site and cloud repositories. Test restoration procedures quarterly.

-   **Disaster Recovery Sites:**\
    Maintain redundant data centers in recommended areas for geographic failover. Replicate systems for minimal downtime.

-   **Continuity Testing:**\
    Conduct annual business continuity exercises simulating major outages to ensure preparedness and validate recovery time objectives and recovery point objectives.

**Insider Threat Mitigation**

-   **Security Awareness Training:**\
    Provide mandatory annual cybersecurity awareness training covering phishing, password hygiene, and reporting suspicious activity.

-   **User Behavior Analytics:**\
    Implement monitoring systems to detect anomalies in user behavior that may indicate insider threats.

-   **Segregation of Duties:**\
    Split responsibilities between system administrators, developers, and auditors to reduce insider abuse risk.

-   **Employee Offboarding:**\
    Immediately disable credentials and recover all assets upon termination.

**Regulatory and Compliance Management**

-   **Policy Alignment:**\
    Align internal policies with HIPAA Security and Privacy Rules, PCI-DSS, and NIST SP 800-53 controls.

-   **Periodic Audits:**\
    Schedule semiannual internal audits and external compliance assessments to ensure continued adherence.

-   **Regulatory Watch:**\
    Have a Compliance Officer to track new legislation or data protection standards that could impact Health Network's operations.

**Emerging Threat Countermeasures**

-   **Email Security:**\
    Deploy Secure Email Gateways with phishing and ransomware filtering.

-   **Endpoint Detection and Response (EDR):**\
    Use Microsoft Defender for Endpoint or similar EDR for behavioral threat detection.

-   **Ransomware Containment:**\
    Segment backup networks, maintain immutable backups, and test ransomware recovery plans.

-   **Threat Intelligence:**\
    Subscribe to CISA alerts for proactive intelligence on new vulnerabilities.

**5. Risk Mitigation Implementation Plan**

  -----------------------------------------------------------------------------------------------------------------------
  **Action Item**                         **Team Responsible**    **Timeline**   **Resources Needed**
  --------------------------------------- ----------------------- -------------- ----------------------------------------
  Implement MFA for all systems           IT Security Team        3 months       Identity management platform, licenses

  Deploy DLP and MDM solutions            Security Operations     6 months       Endpoint protection

  Conduct quarterly vulnerability scans   Security & Compliance   Ongoing        Nessus or Qualys licenses

  Backup validation testing               Infrastructure Team     Quarterly      Backup management tools

  Security awareness training             HR & Security           Annually       eLearning platform

  Disaster recovery simulation            IT Operations           Annually       DR site and testing resources
  -----------------------------------------------------------------------------------------------------------------------

**6. Monitoring and Continuous Improvement**

-   Reviewing the Risk Register quarterly.

-   Updating controls after major incidents, audits, or technology changes.

-   Measuring risk reduction using metrics such as Mean Time to Recover, incident frequency, and patch compliance rates.

-   Reporting results to senior management through a quarterly risk dashboard.

**7. Conclusion**

This Risk Mitigation Plan provides Health Network with a good approach to reducing cybersecurity, operational, and compliance risks. Through technical safeguards, procedural controls, and continuous monitoring, the organization will enhance its resilience against both internal and external threats. Commitment from executive leadership, IT staff, and all employees is essential to a strong foundation and ensuring the protection of Health Network's critical assets, customers, and reputation.

**Business Impact Analysis (BIA) - Health Network**

**Introduction**

This BIA identifies critical data center, supported services, evaluates the business impacts of disruption, and sets recovery objectives to inform continuity planning. The analysis reflects the scenario that winter storms can prevent staff from reaching the Arlington, VA corporate office, that VPN connectivity exists between production data centers and corporate locations, and that certain corporate systems (payroll/accounting) in the office currently lack backups. The BIA focuses on the production data centers while acknowledging corporate-office dependencies and constraints.

**1. Purpose & Objectives**

Determine which data center supported services are most critical to Health Network's mission and operations.

Analyze operational, financial, regulatory, and reputational impacts of outages.

Set recovery requirements: Recovery Time Objective (RTO) and Recovery Point Objective (RPO).

Provide prioritized recovery sequencing to guide continuity and incident response.

**2. Scope & Boundaries**

In scope: Production data center services (compute/virtualization, databases, storage, identity/IAM, network/security edge, remote access, monitoring).

Out of scope: Detailed corporate-office BCP procedures; however, corporate context (Finance, Legal, Customer Support; payroll/accounting located in Arlington) and VPN dependencies are considered.

Disruption scenarios considered: Office inaccessibility due to winter storms; loss of a data center; inter-site network/VPN failures; cyber incidents impacting data center services.

**3. Method & Assumptions**

Qualitative impact ratings (High/Medium/Low) across: safety/trust, revenue/cash flow, legal/regulatory, operations/productivity, and reputation.

Senior leadership has funding and supports participation in BIA/BCP efforts; SMEs are available for inputs/interviews.

Each corporate location can access the others; VPNs exist between data centers and corporate offices.

Corporate payroll and accounting have no current backups and reside only at Arlington; this elevates business impact if access is interrupted.

This BIA uses the given scenario only; figures and targets are fit-for-purpose estimates pending validation during tabletop/exercises.

**4. Impact Categories & Scale**

Safety & Trust: Potential to impact patient/customer safety or erode trust.

Revenue & Cash Flow: Immediate/near-term revenue loss, delayed payments, or additional costs.

Legal/Regulatory: Compliance exposure and penalties (e.g., HIPAA/PCI) and contractual SLAs.

Operations & Productivity: Service desk load, manual workarounds, staff idle time.

Reputation & Brand: Public perception, media scrutiny, executive visibility.

Scale: High (H), Medium (M), Low (L).

**5. Critical Data Center--Supported Services**

  -----------------------------------------------------------------------------------------------------------------------------------------------------------
  Service/Function                    Description
  ----------------------------------- -----------------------------------------------------------------------------------------------------------------------
  Application Hosting Platform        Runs customer- and partner-facing applications; supports APIs and web portals; underpins core service delivery.

  Database Services                   Structured data storage for applications; transactional integrity and reporting.

  Identity & Access (IAM/SSO/PKI)     Authentication, authorization, certificates; required for admins, applications, and corporate access to DC resources.

  Network & Security Edge             Firewalls, VPN gateways, load balancers, WAF/IDS; Internet connectivity and inter-site routing.

  Storage & Backup/Recovery           Block/object storage for VMs and data; snapshots and backup/restore tooling.

  Monitoring, Logging, SIEM           Service health, metrics, log collection, alerting, incident triage.

  Remote Access & OOB Management      Secure remote administration (incl. out‑of‑band) for SRE/NetOps/DBAs, especially when offices are inaccessible.
  -----------------------------------------------------------------------------------------------------------------------------------------------------------

**6. Impact Analysis by Function**

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Function                          Safety/Trust   Revenue/Cash   Legal/Reg   Operations   Reputation   Rationale
  --------------------------------- -------------- -------------- ----------- ------------ ------------ --------------------------------------------------------------------------------------------
  Application Hosting Platform      H              H              H           H            H            Outages halt customer/partner services; SLA penalties; cascading impacts on all teams.

  Database Services                 H              H              H           H            H            Data unavailability corrupts app behavior and reporting; high compliance and revenue risk.

  Identity & Access (IAM/SSO/PKI)   H              H              H           H            H            Admins and apps cannot authenticate; recovery of other services blocked.

  Network & Security Edge           H              H              H           H            H            Loss of Internet/VPN/WAF disrupts all external access and inter-site traffic.

  Storage & Backup/Recovery         H              H              H           H            H            No restore path; risk of data loss; ransomware resilience reduced.

  Monitoring, Logging, SIEM         M              M              M           H            M            Blind to failures/incidents; slower MTTR; increased compliance/reporting risk.

  Remote Access & OOB Mgmt          H              M              M           H            M            Without remote control during storms, response is delayed even if DC services run.
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**7. Recovery Requirements: MAO, RTO, RPO**

Targets reflect business criticality, regulatory drivers, and technical feasibility. MAO = Maximum acceptable outage (also called maximum tolerable period of disruption), RTO = time to restore service, RPO = maximum tolerable data loss (age of last recoverable data).

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Function/Service                  MAO          RTO          RPO          Rationale
  --------------------------------- ------------ ------------ ------------ ---------------------------------------------------------------------------------------------------
  Identity & Access (IAM/SSO/PKI)   4 hours      1 hour       15 minutes   Foundation for all auth; delays block restoration of every other service.

  Network & Security Edge           4 hours      1 hour       15 minutes   Internet/VPN/WAF are prerequisites for external access and inter-site failover.

  Database Services                 6 hours      2 hours      15 minutes   Transactional integrity requires near‑real‑time replication and fast recovery.

  Storage & Backup/Recovery         6 hours      2 hours      15 minutes   Enables restores and ransomware recovery; supports DB/app RPOs.

  Application Hosting Platform      8 hours      2 hours      30 minutes   Resume customer/partner services quickly; drain queues without loss.

  Monitoring/Logging/SIEM           24 hours     8 hours      4 hours      Temporary degradations acceptable; must return to support detection/forensics.

  Remote Access & OOB Mgmt          4 hours      1 hour       N/A          Access capability must be available during office closures; aims for continuity of admin control.
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**8. Critical Resources & Dependencies**

Facilities & Utilities: Co‑location power, cooling, cross‑connects; diverse ISPs.

Technology: Virtualization clusters, storage arrays, DB clusters, CA/PKI, DNS/DHCP/IPAM, firewalls, VPNs, load balancers, WAF/IDS, SIEM.

Data: Production databases, configuration repositories, secrets/keys, machine images.

People: SRE/Infra, NetOps, SecOps, DBAs, App Owners; on‑call with remote access when Arlington is inaccessible.

Third Parties: Payment processors (if applicable), external DNS/CA, circuit providers.

Corporate Dependencies: Finance/Legal/Customer Support rely on VPN/SSO into DC for operations; payroll/accounting currently lack backups and reside in Arlington.

**9. Workarounds & Minimum Service Levels**

Enable queueing with retention for inbound requests until DB/app services recover (to meet RPO without data loss).

Use pre‑approved remote admin jump hosts and out‑of‑band management when corporate offices are closed by storms.

**10. Recovery Priorities & Sequencing**

Phase 1: Network & Security Edge; Identity & Access; Remote Access/OOB.

Phase 2: Storage & Backup/Recovery; Database Services.

Phase 3: Application Hosting Platform and external interfaces/APIs.

Phase 4: Monitoring/Logging/SIEM and reporting dashboards; backlog reconciliation.

Phase 5: Validate corporate VPN/SSO access for Finance, Legal, and Customer Support.

**11. Key Gaps & Requirements**

Backups for corporate payroll/accounting must be implemented with defined RPO/RTO and tested restore procedures.

Document cross‑site failover runbooks and test regularly to achieve the targets above.

Map and validate single points of failure (identity, DNS, certificates, payment gateways, ISP diversity).

**12. Review & Maintenance**

Review this BIA at least annually and after material changes (new apps, architecture shifts, major incidents, audits).

Re‑validate MAO/RTO/RPO during exercises/tabletops and adjust targets based on observed recovery performance.

Track corrective actions from tests and incidents to closure.

**Sources:**

-   U.S. Department of Health & Human Services. (2020). *Summary of the HIPAA Security Rule*. https://www.hhs.gov/hipaa

-   Payment Card Industry Security Standards Council. (2023). *PCI DSS Quick Reference Guide*. https://www.pcisecuritystandards.org

-   Federal Trade Commission. (2023). *FTC Safeguards Rule*. https://www.ftc.gov

-   European Union. (2016). *General Data Protection Regulation (GDPR)*. <https://gdpr-info.eu>

-   National Institute of Standards and Technology. (2012). *Guide for Conducting Risk Assessments (NIST SP 800-30 Rev. 1)*. Retrieved from: [https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-30r1.pdf](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-30r1.pdf?utm_source=chatgpt.com)

-   AuditBoard. (n.d.). *What is a Risk Assessment Matrix?* Retrieved from: [https://auditboard.com/blog/what-is-a-risk-assessment-matrix](https://auditboard.com/blog/what-is-a-risk-assessment-matrix?utm_source=chatgpt.com)

-   Safran. (n.d.). *Introduction to Qualitative Risk Analysis*. Retrieved from: [https://www.safran.com/content/introduction-qualitative-risk-analysis](https://www.safran.com/content/introduction-qualitative-risk-analysis?utm_source=chatgpt.com)

-   Cybersecurity and Infrastructure Security Agency (CISA). *Mitigation Guide for the Healthcare and Public Health (HPH) Sector.* U.S. Department of Homeland Security, 2023, [https://www.cisa.gov/resources-tools/resources/mitigation-guide-healthcare-and-public-health-hph-sector](https://www.cisa.gov/resources-tools/resources/mitigation-guide-healthcare-and-public-health-hph-sector?utm_source=chatgpt.com).

-   Payment Card Industry Security Standards Council. *Payment Card Industry Data Security Standard (PCI DSS) v4.0.* Mar. 2022, <https://www.pcisecuritystandards.org/document_library>.
