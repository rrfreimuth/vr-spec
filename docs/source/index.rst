########################
Variation Representation
########################

Maximizing the personal, public, research, and clinical value of genomic information will require
that clinicians, researchers, and testing laboratories exchange genetic variation data reliably.
The Variant Representation Specification (VR-Spec)–written by a partnership among national information
resource providers, major public initiatives, and diagnostic testing laboratories–is a proposed
open (Apache 2.0) specification to standardize the exchange of variation data.

Here we document the primary contributions of this specification for variant representation:

* **Terminology and information model.** Definitions for biological terms may be abstract or
  intentionally ambiguous, often accurately reflecting scientific uncertainty or understanding at
  the time. Abstract and ambiguous terms are not readily translatable into a representation of
  knowledge. Therefore, the specification begins with precise computational definitions for
  biological concepts that are essential to representing sequence variation. The VR-Spec
  information model specifies how the computational definitions are to be represented in fields,
  semantics, objects, and object relationships.
* **Machine readable schema.** To be useful for information exchange, the information model should
  be realized in a schema definition language. The VR-Spec schema is currently implemented using JSON
  Schema, however it is intended to support translations to other schema systems (e.g. XML,
  OpenAPI, and GraphQL). The schema repository includes language-agnostic tests for ensuring schema
  compliance in downstream implementations.
* **Globally unique computed identifiers.** This specification also recommends a specific algorithm
  for constructing distributed and globally-unique identifiers for genetic states. Importantly, this
  algorithm enables data providers and consumers to computationally generate consistent, globally
  unique identifiers for variation without a central authority.
* **A reference implementation.** We provide a Python package (VR-python) that implements the above
  schema and algorithms, and supports translation of existing variant representation schemes into
  VR-Spec for use in genomic data sharing.
  The machine readable schema definitions and example code are available online at the VR-Spec
  repository (https://github.com/ga4gh/vr-schema).

New to VR-Spec? Start :doc:`here <terms_and_model/terms_and_model>`, or browse the Specification below.

.. toctree::
   :maxdepth: 4
   :caption: VR Specification

   terms_and_model/terms_and_model
   schema
   computed_identifiers
   implementations
   appendices/release_cycle
   appendices/design_decisions
   appendices/planned_extensions
   appendices/todo