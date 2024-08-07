# Enterprise Architecture Framework Principles ( thoughts / draft ).

Focus is on high level principles...

## For all systems and services:

### 1. Security by design

- Integrate security practices throughout the development lifecycle, not as an afterthought, reference: [ACSC Secure-by-Design](https://www.cyber.gov.au/resources-business-and-government/governance-and-user-education/secure-by-design)
- Ensure service providers meet the [Minimum Viable Secure Product](https://mvsp.dev/) baseline, and additional security controls from the [WA Cyber Security Policy](https://www.wa.gov.au/government/publications/2024-wa-government-cyber-security-policy) if needed by the organisations risk assessment.

### 2. Privacy by design

- Embed privacy protections into the design and architecture of IT systems and business practices from the outset, not as an afterthought, reference [OAIC Privacy by design](https://www.oaic.gov.au/privacy/privacy-guidance-for-organisations-and-government-agencies/privacy-impact-assessments/privacy-by-design) and [WA Privacy and Responsible Information Sharing](https://www.wa.gov.au/government/privacy-and-responsible-information-sharing).

### 3. Data Classification and Handling

- Classify information based on sensitivity and implement appropriate handling procedures throughout the data lifecycle, reference [WA Information Classification Policy](https://www.wa.gov.au/government/publications/western-australian-information-classification-policy)

### 4. Align investment to risk and market capabilities

- Systematically migrate legacy systems to modern, low-risk environments with reduced technical debt, prioritising based on business value and risk assessment, reference [ACSC Managing the Risks of Legacy IT: Executive Guidance](https://www.cyber.gov.au/resources-business-and-government/maintaining-devices-and-systems/system-hardening-and-administration/legacy-it-management/managing-risks-legacy-it-executive-guidance)
- Re-use or acquire systems where existing or commercial options closely match business needs
- Develop systems where commercial options are limited or would require significant tailoring to meet business needs

### 5. Adopt [CNCF Cloud-native](https://github.com/cncf/toc/blob/main/DEFINITION.md) practices

- Architect loosely coupled systems that interoperate in a manner that is secure, resilient, manageable, sustainable, and observable. 
- Use automation and the above practices to enable your organization to make high-impact changes frequently, predictably, with minimal toil and clear separation of concerns.

## For organisation developed systems:

### 6. Ownership and Open Source Licencing

- Retain ownership of code and artifacts developed with public funding and use the [Apache 2.0 license](https://www.apache.org/licenses/LICENSE-2.0) to enable broad use, modification, and distribution while limiting legal liability.

### 7. Microservices architecture

- Design applications as collections of loosely coupled, independently deployable services, reference [Microservices Patterns](https://microservices.io/patterns/index.html)
- Adopt [Service meshes](https://landscape.cncf.io/guide#orchestration-management--service-mesh) to add reliability, observability, and security features uniformly across all services on a platform layer without touching the app code. They are compatible with any programming language, allowing development teams to focus on writing business logic.
- Develop and document APIs according to the [OpenAPI Specification](https://spec.openapis.org/oas/latest.html) to ensure consistency, clarity, and interoperability

### 8. Containerization and orchestration

- Package applications and dependencies into containers for consistency and portability, reference [CNCF Application Definition & Image Build](https://landscape.cncf.io/guide#app-definition-and-development--application-definition-image-build)

### 9. Continuous Integration & Delivery

- Automate watching source code for changes, automatically building and testing the code, then begin moving it from development to production where it has to pass a variety of tests or validation to determine if the process should continue or fail, reference [CNCF Continuous Integration & Delivery](https://landscape.cncf.io/guide#app-definition-and-development--continuous-integration-delivery)