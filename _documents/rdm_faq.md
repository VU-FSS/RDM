---
title: VU FSS RDM FAQ
date: 15-02-2023
---

# General

## Where can I go with questions about Research Data Management?
Either the Faculty Data Steward (Koen Leuveld, k.leuveld@vu.nl) or the Library’s RDM Support Desk: rdm@vu.nl. The Data Steward can help you best with questions that are specific to the work we do at the faculty, and with questions about specific grants; the RDM Support Desk is best equipped to deal with questions that could be asked by any VU researcher, for example about storage or archiving options. But both work together, so you can’t ask the wrong person.

## Where can I find more information about Research Data Management?
We maintain a number of resources you can consult. At the VU level, there is the [Research Data Support Portal][rds-portal] which contains links to anything you might want to know about RDM, and the library maintains a series of [Libguides][libguide] explaining various topics related to the management of your data. At the faculty level, the data steward maintains [a page giving advice that is specific to researchers in Social Sciences][fss-rdm-info], including links to content you can use in proposals.

## I don’t have data. I only have observations.
As RDM experts, we would say that observations are also a type of data. But that doesn't really matter: in any case, you want to protect your observations, make backups of your observations and make sure that they are archived securely or shared with the world so that you can demonstrate you did your research well. That is, many important aspects of Research Data Management apply whether you call your observations data or not.

# Data Storage and Security

## Where should I store my data?
Our advice is to use [Yoda][yoda] for storage and archiving, even for sensitive data, and only use VU-managed to devices to access the data. You can find other options in the [Storage Finder][storage-finder], but check with the [Data Steward][datasteward] if they work for the sensitivity level of your data.

## What is the difference between data storage and archiving?
Data storage refers to where you save your data during the research. Your data storage option needs to be available to all collaborators, while still ensuring a sufficient level of security.

Data archiving is where you keep your data after you're done with it, but it may need to be accessed when there are doubts about research integrity. Your data archiving solution can be publically accessible if there is no sensitive data, or restricted-access if there is. The solution needs to be permanent and secure, so that the data cannot be changed, and any links to it will remain functional indefinitely. 

## What security measures should I take?
When using personal data (see below), per GDPR you should take "appropriate organizational and technical measures" to secure your data. The specific actions you should take are not set in stone; you should consider the potential consequences of a data breach, and whether or not the actions you would have to take to prevent them are reasonable.

All VU storage solutions offer a number of security measures. For example, access is only allowed using passwords and multi-factor authentication. If your data is sensitive, there is a number of additional security measures you can take that reduce the risk of data leak, either by reducing the chance a leak happens, or by reducing the impact of a leak.

- Make sure people only have access to the data they need to do their task in your project. For example, with Research Drive it is possible to give each collaborator only access to the folders they need.
- Don't sync data from your Research Drive to your personal computer if you don't have to. For example, once you are done with your raw data, having it on your personal computer only increases the chance that your data is leaked: keep the raw data online-only, and only sync the processed (pseudonymized) data you are working on.
- Make sure everyone in your project is trained in security procedures, such as strong passwords, not clicking attachments in emails from unknown senders etc.
- Pseudonymize your personal data by removing any direclty identifying information, so that any data that is leaked is less likely to be linked to your respondents. If you need to keep the directly identifying data (for example, because it's part of your raw data which you want to keep to demonstrate the provenance of your data, or because you need to contact participants for follow-up), make sure this data will not be leaked at the same time as the pseudonymized data. You can do this either by storing it separately or by encrypting it. See "When should I pseudonymize?", below.
- Encrypt your data, so that if someone accesses the hard drive your data is on they can’t read the data. Software such as [Cryptomator][cryptomator] makes encryption very convenient. Encryption does have a large downside: loss of your password means loss of the data. You can use a password manager to minimize this risk, but it is wise to think twice before deciding to use encryption. 

For help on deciding what measures are appropriate for your data, and with the practical implementation of any of these, you can contact your [data steward][datasteward].

# Personal Data

## What is personal data?
Personal data is any data that can be directly or indirectly linked to a living person. You can directly link data to a person if a direct identifier like their name, phone number, email address etc. is included in the data. You can indirectly link the data if you can combine the data with another piece of data or information to find the person who the data is about. This is possible for more data than you think, so if you collected data from people, it’s safe to assume your data is personal data, even if you remove things like names, phone numbers and addresses.

## What is the difference between anonymization and pseudonymization?
Both these terms mean that you make it less likely that the data that you have can be linked to your respondents, increasing the security of your data. In case of pseudonymization, you remove the possibility of directly linking the data to your respondents, by removing things like names and addresses from the data. Anonymization removes entirely the possibility of linking your data to your respondents, both directly and indirectly. This means that the data is no longer personal data, and GDPR does not apply. However, anonymization is difficult and we don’t usually recommend it (see below).

## When should I pseudonymize?
There is no "one-size-fits-all" answer to this: in general, we do recommend pseudonymizing your data, but in some cases the benefits of pseudonymization may not outweigh the costs. These costs and benefits depend on the nature of your data. A tabular data set is easily pseudonymized by dropping certain variables and generating random identifiers, so it should probably be pseudonymized. On the other hand, for an audio recording it may be practically impossible to edit out all the names. Likewise, the benefits differ; for a dataset containing speeches by famous politicians, leaving out the names will not make identification appreciably more difficult, and yield no security benefits as the data is publicly available anyway. Whether the costs of pseudonymization outweigh the benefits thus depends on the specific project. If you feel the costs don’t outweigh the benefits, feel free to contact your [Data Steward][datasteward] to see if they agree, and make sure to write down your reasoning in your Data Management Plan.

## Should I keep my unpseudonymized data? If so, where?
Ideally, directly identifying data is kept completely separate from research data; in these cases you should destroy the directly identifying information as soon as you can. However, it is often included within the raw data itself. In these cases you should not destroy the data, because you should keep and unedited version of your data for transparency purposes. This raw copy of the data should be stored safely, and in such a way that a data breach doesn't necessarily mean a breach of both pseudonymized and unpseudonymized data. Examples are:

- Store the raw data on a separate server (however, most research programs don't have two servers available).
- Store both raw and pseudonymized data on the same server (or device) but encrypt the raw data. You should make sure that you can't lose your encryption password, or else you lose your raw data.
- Keep both both pseudonymized data on the same server, but make sure the raw data is never synced to personal computers or other devices (for example by adding it to a Yoda Vault). This way, the raw data is protected from the most common data breaches (e.g. losing a laptop in the train).

## Why is it so hard to anonymize data?
Anonymization is potentially very attractive because it removes the need to comply with GDPR. However, it is difficult to combine with the goals of researchers in practice. This is because it will almost always involve making data less detailed, which will harm your ability to draw conclusions from the data. 

To see why, first consider a quantitative data set about work satisfaction, containing gender and age of all respondents. If I know my colleague is a respondent in this survey, I may be able to infer things about my colleague from the public data set. If only one person in the data set matches his age and gender, I have successfully (indirectly) identified him in the data set. If there are multiple people matching his age and gender are present, but none has indicated liking their colleagues, I have still inferred something about him, and may become very disappointed! To prevent me from identifying of my colleague, you as the researcher should thus ensure that there are no unique combinations of age and gender (for example by using broader age bins) and that within each combination of age and gender there is sufficient variation in answers that nothing can be inferred about individuals (so there is always a mix of people who like their colleagues and those who don’t). It is easy to see how the binning of variables may lead to less precision in the analysis, and how difficult it is to ensure that proper variation exists in all (combinations of) variables. There are ways to do this, but it is usually more attractive to keep the data as personal data, even if this puts restrictions on data use due to GDPR.

Qualitative data sets are usually so rich that all observations are unique, and thus potentially identifiable by someone who knows your respondents well (or otherwise has detailed information on them). Qualitative data is therefore usually impossible to fully anonymize, though pseudonymization may be possible.


## I know it's difficult, but I would still like to anonymize my data, how do I do this?

That's great! A good place to start is the R package [sdcMicro][sdcmicro]. Your [data steward][datasteward] may be able to help out when using it. Alternatively, there is [Amnesia][amnesia]. Note that anonymization means modifying your data, so if you want to anonymize data for replication purposes, not all analyses that you did with your unanonymized data can be fully replicated using anonymized data. This is acceptable, if explained properly in your paper (e.g. in a footnote).

## I don’t have informed consent forms for my research. Is that bad?
It’s not necessarily bad, because written informed consent is only required by law in cases of health research (where WMO applies). You can have participants give informed consent orally if you’re not doing WMO research, but make sure you record it and store it safely. You can ask advice from your data steward or privacy champion if you will ask oral informed consent. There are also other legal grounds (than informed consent) on which you can do research. However, if you should have asked informed consent, but did not do so, that could be bad and we recommend that you contact your privacy champion as soon as possible.

# Sharing Data and Notes

## Can I publish personal data?
Yes you can. But make sure:

- Your respondents have given explicit consent to publishing the data; 
- To use VU provided services, such as OSF, Yoda or DataverseNL;
- Not to publish more than needed. In particular, the data should be pseudonymized; and,
- You publish nothing sensitive, and your respondents run no risk because of the data you publish.

## I don’t want to share my data, because participants in my research (or other people) may get in trouble.
In that case, it is not ethical to share them and we recommend that you do not do so. It is still important to archive your data for verification purposes. The [Yoda][yoda] Vault exists for this exact purposes: data stored there can only ever be accessed by other researchers who have a reasonable request for verification. In your DMP you can outline your reasoning why you don’t want to share your data.

## Nobody else but me will understand my notes. Then why should I share them with others?
If your notes contain personal data, you should not probably not share them at all, but you should still archive them so that it can be verified that your research has been done in the way you claim in your publications. If the notes do not contain personal data, sharing your notes is a good way of opening up your research. It’s best not to assume no one is interested in your notes. Even if you think your notes are unreadable, someone may still find them of great use.  For example, someone who wants to do research into how researchers take notes, or someone studying early 21st century hand writing. If you want to share your notes in a more useful and readable way, but are worried about the workload you could also consider cleaning up only a subset of them and sharing that. Little steps to more transparent science can very worthwhile!

## In the informed consent forms, I didn’t ask if data may be reused by other researchers. Can I share them now?
In this situation, you cannot share the personal data with researchers outside the VU. There are two things that you could do:

- If possible, go back to your participants and ask them if other researchers may reuse their data;
- If this turns out to be impossible, anonymize the data. Then the data are no longer personal. We do recommend that you ask your [data steward][datasteward] for help, because this can be tricky (see above: Personal Data > Why is it so hard to anonymize data?).

If neither these are possible, you can’t share the data. This is one of the reasons why it’s so important that you write a Data Management Plan before collecting data, so you will have thought of these things in advance.

## Can I be forced to publish my data because of the WOB?
The Wet Openbaarheid van Bestuur (WOB) only applies to public entities, so not to the Stichting VU (the VU is unique among Dutch universities in this). However, the WOB may apply to the commissioner of your research, for example if your research is commissioned by the national government, or about the functioning of local governments or the police. In these cases, the WOB most likely still doesn’t apply to research data, since there are numerous grounds for exemption, such as the protection privacy. Get in touch with your Data Steward if you’re still worried about this.
I’m afraid that other researchers will misuse my data. How can I prevent that from happening?
It depends on what you mean by “misuse”. If this concerns using your data commercially, you can add a license to your data that specifies non-commercial use only. The same goes for data that may not be remixed. If, however, the misuse can occur simply by the nature of your data, then we recommend that you speak to a data steward and/or a representative of the ethical review committee to discuss your doubts and your options.

# Data Management Plans (DMPs) and FAIR Data

## How can I start writing a Data Management Plan?
You can log into [DMPOnline][dmponline] with your VU credentials to start writing a DMP. It has templates of most funders which are kept up to date by the university library. If you need any help (for example with the technical terms used in many DMP templates), feel free to contact the faculty data steward.

## Where can I find examples of Data Management Plans?
[DMPOnline][dmponline] has a large number of Data Management Plans from which you can get inspiration for your own DMP.

## I never created a Data Management Plan. Is that bad?
There are some situations in which writing a DMP is mandatory. For example, if you have received a grant, you almost always have to write a DMP. The Faculty of Social Sciences also requires you to write a DMP for any new research project you start. And DMPs are sometimes necessary components of various requests, such as an ethics application (for a full procedure) and a storage application (in some cases). And obviously, if you are following the course “Writing a DMP”, you have to write a DMP to complete the course.

Now, for research that is already underway, writing a DMP is a good practice, but not doing so is not necessarily bad. Writing a DMP, though, is a good way to keep you accountable and not let things come down to chance and luck. And it helps you to avoid last-minute panic. Although you are already under way with the research, it can still be a good idea to write a DMP. You can get in touch with your data steward or the RDM Support Desk if you still want to do it.

## What does FAIR data stand for?
FAIR stands for Findable, Accessbile, Inter-operable, and Re-usable. Many of these sub-elements of FAIR cover a wide spectrum of possibilities: some data can be made more easily accessible than others, for example. Below are some tips on how to ensure that your data is acceptably FAIR. 

- Findable: your data needs a persistent identifier, and be registered on a public page somewhere. At the very least, your dataset should be registered on the VU Research Portal (PURE). Here you should also include a DOI link to the data set if your data is publically available. 
- Accessible: make sure that people can access the data in case its needed even if you have changed jobs data and the email address printed on articles you published no longer works. You do this by archiving the data in a repository when you publish findings. This doesn’t need to be a public repository, but your data needs to be at least available for verification purposes, in case there’s doubts about scientific integrity. DarkStor or a Yoda vault both work for this, without publishing data. Public repositories may offer restricted access, where you control who accesses the data, or public access.
- Inter-operable: make sure that if someone has access to your data, they can make use of it (potentially even combine it with other data, if you choose to give people that option). Make sure to use standard file extensions and make sure the data is accompanied by enough information that a well-informed colleague can start using the data without to many difficulties. At a minimum, you should include a Readme file, and any tools used to generate the data (topic lists, questionnaires, interviewer guides, manuals, cleaning scripts etc.). 
- Re-usable: make sure that if people have access to your data, they know what they are allowed to do with it. This means that the terms of use of all outputs are clear, for example by using licenses (as open as possible is best, for example the CC0 license), and that information about the informed consent procedure is included, so other researchers know what your respondent consented to. For using data from DarkStor, a strict data sharing agreement is needed, limiting the use to verification of the research findings.

## My funder wants me to make my data FAIR, but I can’t share the data because of privacy concerns
This is not a problem. Data needs to be Accessible. This means that there is a well-defined procedure for accessing the data, for example in cases where there are doubt about scientific integrity. Storing your data securely on DarkStor is sufficient for this.


<!--LINKS-->

<!--LINKS-->


<!-- Contacts -->

[rdmsupport]: mailto:RDM@vu.nl 
[datasteward]: mailto:k.leuveld@vu.nl
[privacychampion]: mailto:k.leuveld@vu.nl



<!-- Faculty Pages -->

[rerc]: https://vu.nl/en/employee/social-sciences-getting-started/research-ethics-review-fss
[self-check]: https://vuletteren.eu.qualtrics.com/jfe/form/SV_6hCj2czIWzboW6V
[fss-rdm-info]: https://vu.nl/en/employee/social-sciences-getting-started/data-management-fss
[fss-archiving]: https://github.com/kleuveld/rdm_pages/blob/fss_rdm_policy/_documents/fss_archiving_guidelines.md
[fss-rdm-policy]: https://assets.vu.nl/d8b6f1f5-816c-005b-1dc1-e363dd7ce9a5/4d95b39d-42d0-49c3-8797-382ed7767549/FSW%20Datamanagementbeleid%20ENG.pdf


<!-- VU-wide Resources -->

[libguide]: https://libguides.vu.nl/rdm
[rds-portal]: https://vu.nl/nl/medewerker/research-data-support


<!-- Tools -->

[dmponline]: https://dmponline.vu.nl
[sdcmicro]: https://sdcpractice.readthedocs.io/en/latest/sdcMicro.html
[amnesia]: https://amnesia.openaire.eu/
[yoda]: https://portal.yoda.vu.nl
[storage-finder]: https://vu.nl/en/research/storagefinder
[cryptomator]: https://cryptomator.org/


<!-- Templates -->

[privacystatement_nl]: https://vunl.sharepoint.com/:w:/s/FSW-OE-ResearchOfficeFSS/ESBLrBcDrLhLpzfiVI8nHmUB76Deu6chNA3xehbSeOnemw?e=OA1jdu
[privacystatement_en]: https://vunl.sharepoint.com/:w:/s/FSW-OE-ResearchOfficeFSS/EYTq4TISYv5ElJJzSRxC7IcByRFwKCzlMy8EAiOvBXpZmw?e=PIN51k
[informedconsent_nl]: https://vunl.sharepoint.com/:w:/s/FSW-OE-ResearchOfficeFSS/ERBn_xahKvlLkDUK-U_tftEBotu01tkqAGJEmek6QaW7bA?e=bzCJmT
[informedconsent_en]: https://vunl.sharepoint.com/:w:/s/FSW-OE-ResearchOfficeFSS/EWwt5dMHAfJNgoKtxCfiwBYBi_vH0cad1g6XIrHhyFPE0g?e=zfMy3k



