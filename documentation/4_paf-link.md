# Layer 2: Public Affairs (paf.link) {#paf-link}

## Proposal & Decision

[TODO] Describe the binome of proposal and decision. 

* The only answer on Proposal can be a Decision.
* (Also explain that it should only be used in the process where the decision becomes authorative (independent of level). For the use of informative decisions see "Information".)
* [TODO] Make examples: Beispiele: BR-Antrag -> BR-Beschluss; Parlamentarischer Vorstoss -> Verabschiedung des parlamentarischen Vorstosses; 

### Class **paf:Proposal** {#Proposal}

paf:Proposal is an rdfs:subClass of prov:Activity

[Translations](https://www.termdat.bk.admin.ch/entry/56995):

* E: proposal
* D: Antrag
* F: proposition
* I: proposta

This is the activity in the process to formally ask for a decision.

#### Property Variant A **paf:hasProposalSubmitter**

paf:hasProposalSubmitter is a rdfs:subProperty of prov:wasAssociatedWith

[Translations](https://www.termdat.bk.admin.ch/entry/109151)

The agent (person or group) which submits the proposal.

<aside class="example">

```turtle
:proposal_1 a paf:Proposal;
    paf:hasProposalSubmitter :submitter_1.
```

</aside>

#### Property Variant B **prov:qualifiedAssociation**

The agent (person or group) which submits the proposal.

<aside class="example">

```turtle
:proposal_1 a paf:Proposal;
    prov:qualifiedAssociation [
        a prov:Association;
        prov:agent :submitter_1;
        prov:hadRole paf:ProposalSubmitter;
        rdfs:comment "submitter_1 is the issuer of this proposoal."@en
    ].
```

</aside>

#### Property Variant C **paf:hasProposalSubmitter**

The agent (person or group) which submits the proposal.

<aside class="example">

```turtle
:proposal_1 a paf:Proposal;
    paf:hasProposalSubmitter [
        a prov:Association;
        prov:agent :submitter_1;
        prov:hadRole paf:ProposalSubmitter;
        rdfs:comment "submitter_1 is the issuer of this proposoal."@en
    ].
```

</aside>

#### Property Variant D **paf:hasProposalSubmitter**

The agent (person or group) which submits the proposal.

<aside class="example">

```turtle
:proposal_1 a paf:Proposal;
    paf:hasProposalSubmitter [
        a prov:Association;
        paf:hasProposalSubmitter :submitter_1;
        prov:hadRole paf:ProposalSubmitter;
        rdfs:comment "submitter_1 is the issuer of this proposoal."@en
    ].
```

</aside>

#### Property **paf:hasProposalReceiver**

### Class **paf:Decision** {#Decision}

paf:Decision is a rdfs:subClass of prov:Activity

Translations

* Entscheid
* décision
* decisione

This is the activity to formally answer the corresponding paf:Proposal.

## Consultation & Comment

* Beispiele: Vernehmlassung; Ämterkonsultation; Mitberichtsverfahren
Konsultation -> Stellungnahme

### Class **paf:Consultation** {#Consultation}

paf:Consultation is a rdfs:subClass of prov:Activity

[Tranlations](https://www.termdat.bk.admin.ch/entry/56977)

* Konsultation
* consultation
* consultazione

### Class **paf:Comment** {#Comment}

paf:Comment is a rdfs:subClass of prov:Activity

[Translations](https://www.termdat.bk.admin.ch/entry/23059)

* Stellungnahme
* avis
* parere ([TODO] check)

## Mandate & Resolution

* Beispiele: Auftrag zur Erarbeitung einer Stellungnahme der BK an ein Departement -> Erledigung in Form eines Antrags an den Bundesrat; Verabschiedung einer Motion durch die Bundesversammlung -> Auftrag an den BR, die Motion umzusetzen; Brief der GPK an den Bundesrat -> Auftrag, der GPK zu antworten*)

### Class **paf:Mandate**

paf:Mandate is a rdfs:subClass of prov:Activity

[Translations](https://www.termdat.bk.admin.ch/search/entry/109134)

* Auftrag
* mandat
* mandato

### Class **paf:Resolution**

paf:Resolution is a rdfs:subClass of prov:Activity

[TODO] resolution comes from terminology of the parlament, potentially, it is better to have a more common term to day "done".

[Tranlations](https://www.termdat.bk.admin.ch/entry/95501)

* Erledigung (Auflösung?)
* resolution
* risoluzione

## Information & Acknowledgement

### Class **paf:Information**

paf:Information is a rdfs:subClass of prov:Activity

[Tranlations](https://www.termdat.bk.admin.ch/entry/380634)

* Information
* information
* informazione

The activity of sending an information.

### Class **paf:Acknowledgment**

paf:Acknowledgment is a rdfs:subClass of prov:Activity