# HEAL Study Overview

*HEAL DSC Core Metadata piece to provide an overview and enable basic discoverability of your HEAL study, especially when your study is registered and indexed on the [HEAL Data Platform](https://healdata.org/landing) where powerful search and discovery tools leverage this core metadata to make your study easily findable. There are general sections, and HEAL-specific sections. HEAL-specific sections have been developed via test use-cases, and are targeted to facilitate surfacing of your study when relevant to a wide variety of stakeholders intensely interested in questions at the heart of HEAL’s mission to concretely address the many facets of the pain and opioid crises and speed solutions that work for affected individuals and communities.  Note that if the study has more than one aim, a single form should be completed and the multi-select answer options should be used to provide information that reflects the whole study, across all aims.*

<div markdown="1" style="background-color:rgba(0, 0, 0, 0.0470588); text-align:left; vertical-align: top; padding:10px 10px; margin-bottom: 10px;">

NOTE:

* There is no CSV template for the Study Overview. 
* Currently, you will complete your Study Overview using a simple interactive web-form, which you will be able to access once you have registered your study on the [HEAL Data Platform](https://healdata.org/landing).
* Head to the following links for instructions on how to register your study, and then to submit your Study Overview form
  
    * [Register your study on the HEAL Data Platform](https://heal.github.io/platform-documentation/study-registration/)
    * [Submit your Study Overview form](https://heal.github.io/platform-documentation/slmd_submission/)


</div>

## Properties

- **`minimal_info`** *(object)*
    - **`study_name`** *(string)*: The title or name of the study. For NIH-funded studies, this will generally be equivalent to the NIH application ID title.
    - **`study_description`** *(string)*: A description of or abstract for the study. For NIH-funded studies , this will generally be equivalent to the NIH application ID abstract text.
    - **`alternative_study_name`** *(string)*: Study nickname, alternative title, abbreviation, or acronym (e.g. many people shorten the name of the HEAL Adolescent Brain Cognitive Development study to ABCD).
    - **`alternative_study_description`** *(string)*: An alternative description of or abstract for the study. - Generally, for studies with an NIH appl id, if this field is filled out, the text will be searchable on the Platform, but the NIH appl id abstract text will be the study description displayed for the study in the Platform study table entry.
- **`metadata_location`** *(object)*
    - **`nih_application_id`** *(string)*: NIH application ID; only applicable if study is funded by NIH.
    - **`nih_reporter_link`** *(string)*: URL link to the NIH application ID NIH RePORTER webpage; only applicable if study is funded by NIH. Refer to *#/definitions/saneUrl*.
    - **`clinical_trials_study_ID`** *(string)*: ClinicalTrials.gov study ID; only applicable if study is a reportable clinical trial and registered on ClinicalTrials.gov.
    - **`data_repositories`** *(array)*: Describe the data repositories to which data or other shareable products produced by the study will be submitted by the study authors and stored for long-term access; one item in this array per repository.
        - **Items** *(object)*
            - **`repository_name`** *(string)*: Name of a repository in which data or other shareable research products are submitted for storage by study author.
            - **`repository_study_ID`** *(string)*: Unique identifier assigned to the study at that repository; usually a number or combination of standard letters and numbers (e.g. study identifiers on ClinicalTrials.gov are generally in the format: NCT12345678).
            - **`repository_persistent_ID`** *(string)*: Unique persistent identifier assigned to the study at that repository; usually a doi.
            - **`repository_citation`** *(string)*: The official citation the repository requests be used to cite the study/data when the study/data is discovered/accessed via the repository; will likely follow the format: Principal Investigator(s). Title. Place-of-Distribution and Distributor, Date-of-Distribution. DOI. version (where distributor will be the repository name).
    - **`cedar_study_level_metadata_template_instance_ID`** *(string)*: ID of the CEDAR HEAL Study-level Core Metadata Template instance created for this study.
    - **`other_study_websites`** *(array)*: any other websites officially associated with this study that provide additional information about the study.
        - **Items** *(string)*: Refer to *#/definitions/saneUrl*.
- **`citation`** *(object)*
    - **`heal_funded_status`** *(boolean)*: Whether or not the study is funded by the NIH HEAL initiative.
    - **`study_collection_status`** *(boolean)*: Whether or not the study is related to a study group or collection(s) by some administrative mechanism, or belongs to a group or collection of studies (e.g. SAMHSA performs a survey called the National Survey of Substance Abuse Treatment Services (N-SSATS) every year; each annual survey may be registered as a separate study that belongs to a collection called the N-SSATS collection).
    - **`study_collections`** *(array)*: If this study belongs to a study group or collection(s), this is the name or identifier of the study group or collection(s) (e.g. SAMHSA performs a survey called the National Survey of Substance Abuse Treatment Services (N-SSATS) every year; each annual survey may be registered as a separate study that belongs to a collection called the N-SSATS collection).
        - **Items** *(string)*
    - **`funding`** *(array)*: Describe the grants and other funding supporting the study; one item in this array per grant/award or funding source.
        - **Items** *(object)*
            - **`funder_name`** *(array)*: Name of a the granting agency or organization funding the study; include sub-agency administrative entity as second element in array if applicable (e.g. National Institute of Health, National Institute on Drug Abuse).
                - **Items** *(string)*
            - **`funder_abbreviation`** *(array)*: Abbreviation for the name of the granting agency or organization funding the study; include abbreviation for sub-agency administrative entity as second element in array if applicable (e.g. NIH, NIDA).
                - **Items** *(string)*
            - **`funder_type`** *(string)*: Type of granting agency or organization funding the study. Must be one of: `['governmental', 'non-governmental, non-profit, not corporate affiliated', 'non-governmental, non-profit, corporate affiliated', 'non-governmental, for-profit']`.
            - **`funder_geographic_reach`** *(string)*: The geographic reach of the granting agency or organization funding the study. Must be one of: `['international', 'national - non-US', 'national - US', 'state - US', 'local - US']`.
            - **`funding_award_ID`** *(string)*: The grant award ID or number. For NIH-funded studies this will be the project or award number and is distinct from the NIH application ID.
            - **`funding_award_name`** *(string)*: The grant award name. For NIH-funded studies this will be the project or award name and is distinct from the name or title associated with the NIH application ID.
    - **`investigators`** *(array)*: Describe the primary and co-investigators of the study; one item in this array per investigator.
        - **Items** *(object)*
            - **`investigator_first_name`** *(string)*: First name of study primary or co-investigator.
            - **`investigator_middle_initial`** *(string)*: Middle initial of study primary or co-investigator.
            - **`investigator_last_name`** *(string)*: Last name of study primary or co-investigator.
            - **`investigator_affiliation`** *(string)*: Institutional affiliation of study primary or co-investigator.
            - **`investigator_ID`** *(array)*: Add a structured identifier(s) for the investigator; one item in this array per structured identifier; e.g. one item for providing ORCID, another for providing RAS passport.
                - **Items** *(object)*
                    - **`investigator_ID_type`** *(string)*: Type of identifier that will be provided. Must be one of: `['internal NIH RePORTER ID', 'doi', 'ORCID', 'eRA Commons ID', 'RAS Passport']`.
                    - **`investigator_ID_value`** *(string)*: Value of the identifier of the type specified by ID_type.
    - **`heal_platform_persistent_ID`** *(string)*: Persistent identifier assigned to the study on the HEAL Platform; probably a HEAL Platform-branded doi.
    - **`heal_platform_citation`** *(string)*: The official citation the HEAL Platform will request be used to cite the study/data when the study/data is discovered/accessed via the Platform; will likely follow the format: Principal Investigator(s). Title. Place-of-Distribution and Distributor, Date-of-Distribution. DOI. version (where distributor will be: Platform via [Repository Name]).
- **`contacts_and_registrants`** *(object)*
    - **`contacts`** *(array)*: Describe the contact person(s) for the study. This is the person(s) who should be contacted for questions about the study; will be auto-set as NIH contact PI(s) if NIH-funded; one item in this array per contact person.
        - **Items** *(object)*
            - **`contact_first_name`** *(string)*: First name of study contact.
            - **`contact_middle_initial`** *(string)*: Middle initial of study contact.
            - **`contact_last_name`** *(string)*: Last name of study contact.
            - **`contact_affiliation`** *(string)*: Institutional affiliation of study contact.
            - **`contact_email`** *(string)*: Institutional email of study contact.
    - **`registrants`** *(array)*: Describe the person(s) who will register the study on the HEAL Platform. This person(s) must be authorized to access the study registration page/process on the HEAL Platform; will be auto-set as NIH contact PI(s) if NIH-funded; one item in this array per registrant.
        - **Items** *(object)*
            - **`registrant_first_name`** *(string)*: First name of study registrant.
            - **`registrant_middle_initial`** *(string)*: Middle initial of study registrant.
            - **`registrant_last_name`** *(string)*: Last name of study registrant.
            - **`registrant_affiliation`** *(string)*: Institutional affiliation of study registrant.
            - **`registrant_email`** *(string)*: Institutional email of study registrant.
- **`data_availability`** *(object)*
    - **`produce_data`** *(boolean)*: Indicate whether or not the study will collect/produce (primary or secondary) data.
    - **`data_available`** *(string)*: If study will collect/produce data, indicate whether all, some, or none of the data will be made available. Must be one of: `['all', 'some', 'none']`.
    - **`data_restricted`** *(string)*: If study will collect/produce data, and make at least some of that data available, indicate whether all, some, or none of the data will have restriction(s) on access beyond acknowledgement and signing of a minimal DSA. Must be one of: `['all', 'some', 'none']`.
    - **`data_collection_status`** *(string)*: If study will collect/produce data, indicate whether the study has not started, has started, or has finished data collection/production activities. Must be one of: `['not started', 'started', 'finished']`.
    - **`data_release_status`** *(string)*: If the study will collect/produce data and make at least some of the data available, indicate whether the study has not started, has started, or has finished data release activities. Must be one of: `['not started', 'started', 'finished']`.
    - **`data_collection_start_date`** *(string)*: If the study will collect/produce data, indicate the anticipated date when data collection/production will begin.
    - **`data_collection_finish_date`** *(string)*: If the study will collect/produce data, indicate the anticipated date when data collection/production will end (data collection/production is complete).
    - **`data_release_start_date`** *(string)*: If study will collect/produce data and make at least some of the data available, indicate the anticipated date when first data will be released.
    - **`data_release_finish_date`** *(string)*: If study will produce data and make at least some of the data available, indicate the anticipated date when last data will be released (data release is complete).
    - **`produce_other`** *(boolean)*: Indicate whether or not the study will produce shareable products other than data.
- **`findings`** *(object)*
    - **`primary_publications`** *(array)*: List of the doi for any/all primary study publications that use the study data; include any papers, books, articles, blog posts, etc. authored by the investigators or team responsible for the study; one item in this array per publication/doi.
        - **Items** *(string)*
    - **`primary_study_findings`** *(array)*: Simple, one-sentence take-away conclusion(s) from study author publications; one item in this array per single-sentence conclusion (e.g. item #1: Provision of MAT rx to men with documented OUD leaving jail reduces overdose risk by 9%; item #2: Provision of MAT rx plus case management support to men with documented OUD leaving jail reduces overdose risk by 30%; item 3: Provision of MAT rx plus case management support to men with documented OUD leaving jail is more effective than provision of MAT rx alone at reducing risk of OUD overdose).
        - **Items** *(string)*
    - **`secondary_publications`** *(array)*: List of the doi for any/all secondary study publications that use the study data; include any papers, books, articles, blog posts, etc. authored by persons OTHER THAN the investigators or team responsible for the study; one item in this array per publication/doi.
        - **Items** *(string)*
- **`study_translational_focus`** *(object)*
    - **`study_translational_focus`** *(string)*: Whether the study is primarily focused on learning more about a human opioid or pain CONDITION or on discovering, or learning more about a TREATMENT OF A CONDITION, intervention, or solution for a human opioid or pain condition. This may be quite simple to infer for human subject studies. For studies not involving human subjects, please consider how/where the study will most substantially contribute to the HEAL Initiative translational purpose of learning more about human opioid and pain conditions and driving development of solutions to these conditions. Note there are some studies that are not related to a specific condition or the treatment of a condition.  An example of a study like this is the National Institute on Drug Abuse (NIDA) study Incarceration Effects on Medicaid Status. If a study like this does not apply to a condition or treatment, this question can be left blank.Choose one. Must be one of: `['Condition', 'Treatment of a Condition']`.
    - **`study_translational_topic_grouping`** *(array)*: What types of determinants and/or mechanisms related to human opioid use or pain conditions is the study investigating and/or measuring (e.g. A study investigating differential pain/nociception signaling in persons living in neighborhoods with high versus low social cohesion might choose both 'Biology and Health' and 'Social Determinants'). Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Biology and Health', 'Mental Health', 'Social Determinants', 'Public Attitudes or Stigma']`.
- **`study_type`** *(object)*
    - **`study_stage`** *(array)*: The high-level category or type/stage of research being conducted.
        - **Items** *(string)*: Must be one of: `['Pre-Research/Protocol Development', 'Basic Research', 'Pre-Clinical Research', 'Clinical Research', 'Implementation Research', 'Post-market Research', 'Business Development', 'Epidemiologic Research']`.
    - **`study_primary_or_secondary`** *(string)*: Is the study collecting data itself to analyze and draw conclusions or is it leveraging data collected by other entities to analyze and draw conclusions. Must be one of: `['Primary Research', 'Secondary Research']`.
    - **`study_observational_or_experimental`** *(string)*: Whether the study is observational (no explicit intervention) or experimental (some explicit intervention). Must be one of: `['Observational Research', 'Experimental Research']`.
    - **`study_subject_type`** *(array)*: What is the actual species or entity that is experimentally or observationally studied in the research; each HEAL study will have translational relevance to humans, but not all HEAL studies directly study humans.
        - **Items** *(string)*: Must be one of: `['Human', 'Animal', 'Human cell/tissue/tissue model', 'Animal cell/tissue/tissue model', 'Molecule (e.g. chemical/protein engineering, protein crystallization)']`.
    - **`study_type_design`** *(array)*: The overarching study type and more granular study design. Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Basic Research - Theory/Modeling', 'Basic Research - Applied', 'Basic Research - Method/Protocol development', 'Basic Research - Animal study', 'Basic Research - Cell study', 'Basic Research - Genetic study', 'Basic Research - Biochemistry study', 'Basic Research - Biophysical study', 'Basic Research - Gene sequencing', 'Basic Research - Genetic Engineering', 'Basic Research - Material Development', 'Basic Research - Device Development', 'Basic Research - Small molecule screen', 'Basic Research - High throughput screen', 'Basic Research - Screen, other', 'Clinical Research - Phase I', 'Clinical Research - Phase II', 'Clinical Research - Phase III', 'Clinical Research - Phase IV', 'Clinical Research - Therapy/drug study without intervention', 'Clinical Research - Case Report or Series', 'Preclinical Research', 'Randomized Control Trial', 'Pre/Post', 'Stepped Wedge', 'Regression Discontinuity', 'Difference in Differences', 'Cross-over', 'Natural Experiment', 'Cohort, prospective', 'Cohort, retrospective', 'Cohort - panel, longitudinal', 'Cohort - cross-sectional, longitudinal', 'Cohort - cross-sectional, single time-point', 'Case control', 'Ecological', 'Monitoring/surveillance', 'Inventory', 'Curation', 'Meta-analysis', 'Review', 'Review, Systematic', 'Review, Simple (narrative)']`.
- **`human_treatment_applicability`** *(object)*
    - **`treatment_investigation_stage_or_type`** *(array)*: If the study is investigating a treatment, intervention, or solution to a human opioid or pain condition, what type of investigation is the study undertaking? at what stage in the treatment investigation process does this study lie?
        - **Items** *(string)*: Must be one of: `['target discovery', 'target mechanism', 'treatment discovery', 'treatment mechanism', 'treatment efficacy', 'differential treatment efficacy', 'treatment implementation', 'treatment availability or accessibility']`.
    - **`treatment_mode`** *(array)*: Is the treatment, intervention, or solution that my study is relevant to meant to prevent the occurrance of a condition (e.g. development of a non-opioid drug for pain to prevent opioid exposure and addiction, case management and MAT for pregnant women to prevent in utero exposure to opioids, safe needle exchange center to prevent spread of blood borne diseases among people using heroin), treat an occurrance of a condition (e.g. naloxone to treat opioid overdose, physical therapy to treat existing pain from a back injury) , and/or is it a harm reduction mechanism (e.g. safe needle exchange reduces harm associated with heroin addiction/use, decriminalization of heroin possession or use reduces the harm associated with heroin addiction/use).
        - **Items** *(string)*: Must be one of: `['Preventive (prevention of an occurrence)', 'Therapeutic (treating an occurrence)', 'Harm Reduction (preventing more of an occurrence, or preventing harm from an occurrence)']`.
    - **`treatment_novelty`** *(array)*: Is the treatment, intervention, or solution that my study is relevant to totally novel, is it totally established, does it have some element of novelty added to an established intervention (novel added to established, established used in a novel population, setting, or combination)? .
        - **Items** *(string)*: Must be one of: `['Novel', 'Novel, added to established', 'Established', 'Established, used in novel population, setting, or combination']`.
    - **`treatment_application_level`** *(array)*: Is the treatment, intervention, or solution that my study is relevant to applied at the individual level (e.g. a doctor prescribes a drug or physical therapy regimen to a patient) or at the population/community/group level (e.g. a city changes good samaritan naloxone laws, or implements a safe needle exchange center, or adds park maintenance resources to the budget to provide more access to outside places to exercise)?
        - **Items** *(string)*: Must be one of: `['Individual', 'Population']`.
    - **`treatment_type`** *(array)*: Classify the treatment, intervention, or solution the study is relevant to by broad type of intervention. Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['drug', 'non-opioid drug', 'opioid drug', 'non-biologic drug', 'biologic drug', 'non-drug', 'device', 'behavioral', 'psychotherapy', 'group therapy', 'physical therapy', 'exercise', 'education', 'community resources/supports', 'economic supports', 'housing supports', 'case management', 'environmental (indoors)', 'environmental (outdoors)', 'law/policy', 'surgical procedure', 'nutritional', 'nutritional supplement', 'gene therapy', 'immunotherapy', 'electrotherapy']`.
- **`human_condition_applicability`** *(object)*
    - **`condition_category`** *(array)*: Considering the study in a translational context, to humans with which broad category(ies) of opioid use or pain conditions are the study results intended to apply. Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Opioid use and opioid use disorder', 'Opioid use and opioid use disorder, primary occurrence', 'Opioid use and opioid use disorder, relapse', 'Opioid use and opioid use disorder, chronic', 'Opioid overdose', 'Opioid exposure', '(Non-opioid) Substance use', 'Co-occurring (Opioid or Non-opioid) Substance use and Mental Health disorder', 'Pain', 'Pain, acute', 'Pain, chronic', 'Pain, acute to chronic transition', 'Pain, resulting from injury', 'Pain, resulting from surgery', 'Pain, resulting from chronic illness', 'Pain, idiopathic (unknown origin)']`.
    - **`condition_investigation_stage_or_type`** *(array)*: Each HEAL study will be doing work that is relevant to a human opioid and/or pain condition. What does this study intend to learn about the condition? If the study is investigating a treatment, intervention, or solution, please choose 'Treatment of Condition'. Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Incidence of condition', 'Risk for condition', 'Differential risk for condition', 'Mechanism of condition', 'Impact of condition', 'Public attitudes towards or perception of condition', 'Treatment of condition']`.
    - **`pain_causal_condition`** *(array)*: If the study will be doing work that is relevant to a human PAIN condition category, is the study focusing on pain caused by a specific condition? e.g. Cancer, fibromyalgia, arthritis, occupational injury, sports injury, car accident, surgical procedure. If yes, please indicate the causal condition(s) here - Values will be restricted to NLM MeSH Diseases - see Branch 'C' here: https://meshb-prev.nlm.nih.gov/treeView.
        - **Items** *(string)*
    - **`pain_treatment_or_study_target_condition`** *(array)*: If the study will be doing work that is relevant to a human PAIN condition category, and the pain condition has a causal condition (specified above), is the study focusing its investigation on the causal condition, or on the pain resulting from the causal condition? e.g. In a study of effective treatments for fibromyalgia/fibromyalgia pain, is the study focused on fibromyalgia disease-modifying treatments, or on treatments that address the symptomology of pain? Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Causal Condition', 'Pain', 'Pain, acute', 'Pain, chronic']`.
    - **`all_treatment_or_study_target_condition`** *(array)*: Considering the study in a translational context, to humans with which detailed type of opioid use or pain conditions are the study results intended to apply? Each HEAL study will be doing work that is relevant to a human opioid and/or pain condition; You indicated the broad category of condition(s) the study is focusing on or relevant to above. Here, please indicate the study focus condition(s) in detail. Choose as many as apply - Values will be restricted to NLM MeSH Diseases - see Branch 'C' here: https://meshb-prev.nlm.nih.gov/treeView.
        - **Items** *(string)*
    - **`all_outcome_condition`** *(array)*: If the outcome condition(s) the study hopes to impact or measure is different than the treatment or study target condition (e.g. testing a disease-modifying fibromyaligia treatment but measuring depression, physical and social function, and neurologic pain such as headaches as the main outcomes). Please indicate the study outcome condition(s) here. Choose as many as apply - Values will be restricted to NLM MeSH Diseases - see Branch 'C' here: https://meshb-prev.nlm.nih.gov/treeView.
        - **Items** *(string)*
    - **`all_other_condition`** *(array)*: If the study is measuring or tracking other human health conditions besides the treatment or study target condition and outcome condition, please indicate the other tracked/measured condition(s) here. Choose as many as apply - Values will be restricted to NLM MeSH Diseases - see Branch 'C' here: https://meshb-prev.nlm.nih.gov/treeView.
        - **Items** *(string)*
- **`human_subject_applicability`** *(object)*
    - **`gender_applicability`** *(array)*: Considering the study in a translational context, to humans of which gender identity(ies) are the study results intended to apply and/or likely to generalize to.
        - **Items** *(string)*: Must be one of: `['Female', 'Female-to-male transsexual', 'Intersexed', 'Male', 'Male-to-female transsexual', 'Other']`.
    - **`sexual_identity_applicability`** *(array)*: Considering the study in a translational context, to humans of which sexual identity(ies) are the study results intended to apply and/or likely to generalize to.
        - **Items** *(string)*: Must be one of: `['Heterosexual', 'Homosexual (gay/lesbian)', 'Bisexual', 'Asexual', 'Other']`.
    - **`biological_sex_applicability`** *(array)*: Considering the study in a translational context, to humans of which biological sexes are the study results intended to apply and/or likely to generalize to.
        - **Items** *(string)*: Must be one of: `['Ambiguous', 'Female', 'Male']`.
    - **`age_applicability`** *(array)*: Considering the study in a translational context, to humans of which age or developmental stage are the study results intended to apply and/or likely to generalize to.
        - **Items** *(string)*: Must be one of: `['Fetus', 'Infant, newborn (Birth to 1 month)', 'Infant (1 to 23 months)', 'Child, preschool (2 to 5 years)', 'Child (6 to 12 years)', 'Adolescent (13 to 18 years)', 'Adult (19 to 44 years)', 'Middle aged adult (45 to 64 years)', 'Aged adult (65 to 79 years)', 'Aged, 80 and over (80 years and over)']`.
    - **`irb_vulnerability_conditions_applicability`** *(array)*: Considering the study in a translational context, which special IRB human vulnerability conditions are the study results intended to address or apply to?
        - **Items** *(string)*: Must be one of: `['Pregnant women', 'Human fetuses', 'Neonates', 'Prisoners', 'Children', 'Individuals with physical disabilities', 'Individuals with mental disabilities or cognitive impairments', 'Economically disadvantaged', 'Socially disadvantaged', 'Terminally ill or very sick', 'Racial or ethnic minorities', 'Institutionalized persons (for example, persons in correctional facilities, nursing homes or mental health facilities)']`.
    - **`geographic_applicability`** *(array)*: For studies with human subjects, from which geographic location(s) are subjects recruited. If subjects are recruited in the US nationally, choose only US - national. If subject are recruited in the US only in specific state(s), choose US - Specific States, then please also select the abbreviation of each of the specific states from which subjects are recruited. If subjects are recruited in the US from specific county(ies) within specific state(s), please choose US - Specific States and US - Specific Counties, and choose the abbreviation of each specific state from which subjects are recruited.
        - **Items** *(string)*: Must be one of: `['Non US', 'US - National', 'US - Specific States', 'US - Specific Counties', 'AK', 'AL', 'AR', 'AZ', 'CA', 'CO', 'CT', 'DE', 'FL', 'GA', 'HI', 'IA', 'ID', 'IL', 'IN', 'KS', 'KY', 'LA', 'MA', 'MD', 'ME', 'MI', 'MN', 'MO', 'MS', 'MT', 'NC', 'ND', 'NE', 'NH', 'NJ', 'NM', 'NV', 'NY', 'OH', 'OK', 'OR', 'PA', 'RI', 'SC', 'SD', 'TN', 'TX', 'UT', 'VA', 'VT', 'WA', 'WI', 'WV', 'WY']`.
- **`data`** *(object)*
    - **`data_orientation`** *(array)*: Does the study produce/collect quantitative data?, qualitative data? Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Quantitative', 'Qualitative']`.
    - **`data_source`** *(array)*: What is the source of the data the study will produce/collect. Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Administrative', 'Government Collected/Measured', 'Clinical/EHR', 'Laboratory', 'Researcher Collected/Measured', 'Patient-Reported']`.
    - **`data_type`** *(array)*: What is the type of the data the study will produce/collect. Choose as many as apply.
        - **Items** *(string)*: Must be one of: `['Genomic', 'Proteomic', 'Biochemical', 'Biophysical', 'Imaging', 'Interview/Focus Group', 'Interview/Focus Group - structured', 'Interview/Focus Group - semi-structured', 'Interview/Focus Group - unstructured', 'Questionnaire/Survey/Assessment', 'Questionnaire/Survey/Assessment - validated instrument', 'Questionnaire/Survey/Assessment - unvalidated instrument']`.
    - **`subject_data_unit_of_collection`** *(array)*: For studies with human subjects, is the data collected at the individual or population level?
        - **Items** *(string)*: Must be one of: `['Individual', 'Community, Group, Cluster, Population']`.
    - **`subject_data_unit_of_collection_expected_number`** *(integer)*: For studies with human subjects, what is the expected number of subjects for which data will be collected? If unit of data collection is individuals this is the expected number of individuals, and if the unit of data collection is populations/clusters this is the expected number of populations/clusters.
    - **`subject_data_unit_of_analysis`** *(array)*: For studies with human subjects, is the data analyzed at the individual or population level?
        - **Items** *(string)*: Must be one of: `['Individual', 'Community, Group, Cluster, Population']`.
    - **`subject_data_unit_of_analysis_expected_number`** *(integer)*: For studies with human subjects, what is the expected number of subjects at the level at which data will be analyzed? If unit of data analysis is individuals this is the expected number of individuals, and if the unit of data analysis is populations/clusters this is the expected number of populations/clusters.
    - **`subject_data_level_available`** *(array)*: For studies with human subjects that will make at least some data available, will data be made available at the individual subject level or some level of aggregation?
        - **Items** *(string)*: Must be one of: `['Individual - Unaggregated', 'Individual - Aggregated', 'Community, Group, Cluster, Population - Unaggregated', 'Community, Group, Cluster, Population - Aggregated', 'Unaggregated', 'Aggregated', 'Aggregated, across all (population summary statistics)', 'Aggregated, by treatment/exposure group', 'Aggregated, by demographic variable(s)', 'Aggregated, by geographic variable(s)']`.
    - **`subject_geographic_data_level_collected`** *(array)*: For studies with human subjects, will geographic data be collected? if so, what level of geographic detail will be collected?
        - **Items** *(string)*: Must be one of: `['Exact location', 'Census block', 'Census tract', 'Zip code', 'County', 'Sub-state region', 'State', 'Multi-state region', 'Nation', 'No geographic data will be collected']`.
    - **`subject_geographic_data_level_available`** *(array)*: For studies with human subjects that collect geographic data and will make at least some data available, will geographic data be made available? if so, what level of geographic detail will be made available?
        - **Items** *(string)*: Must be one of: `['Exact location', 'Census block', 'Census tract', 'Zip code', 'County', 'Sub-state region', 'State', 'Multi-state region', 'Nation', 'No geographic data will be made available']`.
## Definitions

- **`saneUrl`**

