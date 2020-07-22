## Open Issues and Questions

Open Issue 1:

What level of portability, availability and openness should be proposed
to access SNIF (such as discovery of the repository, access to, and
searching within the repository)? We recognize a trade-off between
accessibility/convenience and exposure of network connectivity details
with access to PHI.

Open Issue 1 response:

There are two aspects to security:

1.  what elements should be included within the form (Open Issue 4) and,

2.  what security controls are required to access the form itself (this
    Open Issue). An initial proposal suggests that ATNA could be
    leveraged a dependency for both issues is included within the
    profile.

Public comment is sought on this approach, as well as additional
security control baselines that should apply to a SNIF data source based
on requirements and guidelines such as:NIST
[800-53](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r4.pdf#page=51),
[MDR 2017/745](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32017R0745),
[EU Directive on Security of Network and Information
Systems](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32016L1148),
[EU
GDPR](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32016R0679),
[EU Cybersecurity
Act](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32019R0881),
[ANSI/NEMA
HN 1-2019](https://www.nema.org/Standards/Pages/manufacturer-disclosure-statement-for-medical-device-security.aspx?key=67ri900e6rt5af#download),
ISO/IEC 27001/2 and
[FIPS 140-3](https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.140-3.pdf)
for US Federal Agencies.

Open Issue 2:

What amount of security information should be included within the data
model without compromising security?

Consider, although not intended as a security tool, SNIF could aid in
aid in a project to [map an existing
network](https://apps.nsa.gov/iaarchive/library/ia-guidance/security-configuration/networks/manageable-network-plan.cfm).

Open Issue 2 response:

An initial proposal suggests that ATNA options could be included within
the data model.

Public comment is sought on this approach, as well as additional data
elements such as:

  - security risk assessment level and/or classification,

  - link to a MDS2,

  - VLAN details (e.g., encrypted VLAN used to secure legacy equipment),

  - CA authority, public key, TLS version and authentication token.

Note: these may duplicate information in an existing security management
database.

Open Issue 3:

How should the data be organized? Should there be 1 form per system or 1
form per site?

Open Issue 3 response:

The form is a virtual form and should allow for one or more; public
comment is sought on this approach.

Open Issue 4:

Are the assumptions regarding an institution’s role in interface
management correct? Initial feedback suggests that institutions tend not
to catalogue endpoints, however there is some interest in having such
information available, in order to become more self-sufficient.

Open Issue 4 response:

Seek public comment on the following:

  - Are interface endpoints catalogued today? If so, who maintains the
    catalogue?

  - If an endpoint catalogue was standardized, would institutions and
    vendors adopt it?

  - Would institutions be willing to transition their current systems to
    one that is standardized?

Open Issue 7:

Regarding a SNIF Profile:

  - Is there a preferred technical approach based on existing standards,
    referenced in Section 2.2 below?

  - Is there any interest from an organization willing to develop an
    opensource implementation as a project related to the SNIF profiling
    activity?

  - Should SNIF have focus on implementation and break-fix use cases, or
    should it take a greater role in routine network transactions (i.e.,
    reference SNIF in lieu of a static host file)?

  - SNIF-like functionality is exercised in the Carequality/eHealth
    Exchange Provider Directory, what Carequality attributes should be
    included in SNIF (and vice-versa)?

Open Issue 8:

SNIF Repositories:

  - How should multiple SNIF Repositories be managed? Is there a need
    for an authoritative Repository and defined data management
    policies? Do Digital Signatures offer a solution? Should only one
    SNIF Repository be allowed (as with an XDS Registry)? See Sections
    4.1and 4.4.3 below.

  - Should the Repository query Content Creators for updates or does
    this add unnecessary complexity (i.e., should bi-directional
    transactions be established as discussed in Section 4.4.2 below)?

Open Issue 9:

To what extent should connectivity details be incorporated in the data
model to differentiate an endpoint without being overly exhaustive?
Noting that the more information that is included, the more of a burden
SNIF can be to maintain. Public comment is sought on:

  - The data element “Period” was borrowed from the FHIR Endpoint
    resource. There are several other timestamps that could be included
    such as: created in repository, last updated in repository, created
    by content creator, last updated by content creator. This could
    reach a tipping point and lend towards recording such information in
    an audit trail. What is the preferred approach for timestamps?

  - Which fields are suited for encoding as identifiers for machine
    readability?

  - Are there recommended standards that can satisfy one or more groups
    of the data model (Administrative, Operational or Technical)? Is
    there a better grouping that enables use of existing standards?

  - How should the data model handle synchronous vs. asynchronous
    services?

Open Issue 10:

How can this profile avoid interfering with facility network
inventory/configuration management systems? Some facilities already
maintain system-wide configuration inventories that identify all network
connected systems, their addresses, identification, etc. These typically
do not capture vendor specific or standards-based interoperability
protocol configurations; they manage network addresses, ports,
make/model, responsible party, etc.

Other facilities will be establishing such systems because this kind of
network management is a basic starting point for all security management
frameworks.

Initial feedback suggests that facilities manage the network layer, not
the application layer, however, further comment is sought on two
potential points of interference:

  - Use of SNIF creates information inconsistency between the facility
    system and the SNIF system. This is usually the result of updating
    one but not the other system.

  - SNIF system could be mis-used as a substitute for a facility system.

## Closed Issues

Closed Issue 1:

Is there incentive for the healthcare institution to own and manage
configuration details? Such details are typically held by vendors and
within vendor systems.

Data can quickly become obsolete through movement within the facility,
upgrades or de-installations; further de-incentivizing institutions to
maintain this information. What model should be used for data
collection? Manual entry is not sustainable.

Closed Issue 1 response:

To reduce, and possibly eliminate the need for healthcare institutions
to create and maintain configuration details, a vendor supported, shared
model is proposed in 4.1 below. This proposes a model in which
connectivity details held within vendor applications are exposed in a
standardized manner. By reducing the resources required to manually
maintain SNIF, we are hoping to incentivize adoption.

Closed Issue 2:

Should the profile include provisions for automated or
self-configuration (e.g., automated XCA-I config, or fully automated
Connectathon setup)?

Closed Issue 2 response:

An interpretation of automated and self-configuration may be found in
Section 4.7 below. The initial scope of this profile is to establish
common content, and a means to access content pertaining to technical
configuration details. Future extensions could include discovery and
automation upon successful adoption of the initial profile.
