---
title: Call for Artifacts
---

# Call for Artifacts

VMCAI 2023 makes available the option to submit an artifact along with a paper. Artifacts are any additional material that substantiates the claims made in the paper, and ideally makes them fully replicable. For some papers, these artifacts are as important as the paper itself because they provide crucial evidence for the quality of the results. The goal of artifact evaluation is twofold. On the one hand, we want to encourage authors to provide more substantial evidence to their papers and to reward authors who create artifacts. On the other hand, we want to simplify the independent replication of results presented in the paper and to ease future comparison with existing approaches. Artifacts of interest include (but are not limited to):

* Software, Tools, or Frameworks
* Data sets
* Test suites
* Machine checkable proofs
* Any combination of them
* Any other artifact described in the paper

Artifact submission is **optional**. However, we highly encourage all authors to also submit an artifact. A successfully evaluated artifact can increase your chance of being accepted since the evaluation result of your artifact is taken into account during paper reviewing. Additionally, badges shown on the title page of the corresponding paper give you credit for good artifact submissions. We award one of three types of badges. For artifacts that are successfully evaluated by the artifact evaluation committee we grant the available badge. Artifacts that are publically available under a DOI receive an availability badge. Authors may use all granted badges on the title page of the respective paper.

## Important Dates

The artifact evaluation will be done in parallel with the evaluation of the submitted paper. The artifacts submission deadline is 1 week after the paper submission.

September 9, 2022: Artifact submission opens

~~September 15, 2022~~ September 22, 2022: Artifact submission

October 3, 2022: Artifact test phase notification

October 4–7, 2022: Artifact clarification period

October 30, 2022: Artifact notification

All artifacts are evaluated by the artifact evaluation committee. Each artifact will be reviewed by at least two committee members. Reviewers will read the paper and explore the artifact to evaluate how well the artifact supports the claims and results of the paper. The evaluation is based on the following questions.

* Is the artifact consistent with the paper and the claims made by the paper?
* Are the results of the paper replicable through the artifact?
* Is the artifact complete, i.e., how many of the results of the paper are replicable?
* Is the artifact well-documented?
* Is the artifact easy to use?

The artifact evaluation is performed in the following two phases.

* In the test phase, reviewers check if the artifact is functional, i.e., they look for setup problems (e.g., corrupted, missing files, crashes on simple examples, etc.). If any problems are detected, the authors are informed of the outcome and asked for clarification. The authors will get 3 days to respond to the reviews in case problems are encountered.
* In the assessment phase, reviewers will try to reproduce any experiments or activities and evaluate the artifact w.r.t the questions detailed above.

## Artifacts Submission

An artifact submission should consist of

* an abstract that summarizes the artifact and explains its relation to the paper including:
* a URL from which a .zip or .tar.gz archive file containing the artifact can be downloaded - we encourage you to provide a DOI
* the SHA256 checksum of the archive file
* a .pdf file of the submitted paper contained within the archive file.

The artifact evaluation chairs will download the archive file and distribute it to the reviewers. Please also look at the Artifact Packaging Guidelines section for detailed information about the contents of the submission. The abstract (as a txt or pdf) should be submitted to submitted to EasyChair. The abstract should include a description of the artifact, the URL of the download link (you should upload your vm to a hosting service of your choice - easychair will not accept vm uploads), as well as the SHA256 checksum of your archive file.

[https://easychair.org/my/conference?conf=vmcai2023ae]()

We need the checksum to ensure the integrity of your artifact. You can generate the checksum using the following command-line tools.

* Linux: `sha256sum <file>`
* Windows: `CertUtil -hashfile <file> SHA256`
* MacOS: `shasum -a 256 <file>`

If you cannot submit the artifact as requested or encounter any other difficulties in the submission process, please contact the artifact evaluation chairs prior to submission.

## Artifact Packaging Guidelines

There are two acceptable ways to submit your artifact. You may either package the artifact as an archive file and write their instructions such that the artifact evaluation committee can evaluate the artifact within a virtual machine provided by us. In this case, only submit the required files to replicate your results in the provided virtual machine. If you submit in this way, you would not submit a virtual machine image in the archive file. AEC members will copy your archive file into the provided virtual machine.

The second option is to modify the given VM and reupload the VM to a hosting platform of your choice. We will check the hash of the image, then load the VM to test your artifact. In this case, a README should be contained in the home directory of the VM.

We recommend preparing your artifact in such a way that any computer science expert without dedicated expertise in your field can use your artifact, especially to replicate your results. For example, provide easy-to-use scripts and a detailed README document.

## VMCAI 2022 Virtual Machine

An initial version of the virtual machine is available [here](https://drive.google.com/file/d/1R0gcoXtxbDUp3xNYsTGBt_nmewXo6ZiI/view?usp=sharing). The user name and password are vmcai. If you have any questions regarding the VM or in case you think the VM is improper for evaluation of your artifact, please contact the artifact evaluation chair.

## Submission Contents

Your virtual machine must contain the following elements.

1. The main artifact, i.e., data, software, libraries, scripts, etc. required to replicate the results of your paper. ◦ The review will be singly blind. Please make sure that you do not (accidentally) learn the identify of the reviewers (e.g., through analytics, logging).
2. A license file. Your license needs to allow the artifact evaluation chairs to download and distribute the artifact to the artifact evaluation committee members and the artifact evaluation committee members must be allowed to evaluate the artifact, e.g., use, execute, and modify the artifact for the purpose of artifact evaluation.
3. A README text file that introduces the artifact to the user and guides the user through replication of your results. Ideally, it should describe the structure and content of your artifact. It should also describe the steps to set up your artifact within the VM. To simplify the reviewing process, we recommend providing an installation script (if necessary). We would appreciate it if you would support the reviewers not only for the main review phase but also for the testing phase. To this end, it would be helpful if you would provide instructions that allow installation and rudimentary testing (i.e., in such a way that technical difficulties would pop up) in as little time as possible.
Document in detail how to replicate your results of the paper:

Please document which claims or results of the paper can be replicated with the artifact and how (e.g., which experiment must be performed). Please also explain which claims and results cannot be replicated and why.

* Describe in detail how to replicate the results in the paper, especially describe the steps that need to be performed to replicate the results in the paper. To simplify the reviewing process, we recommend providing evaluation scripts (where applicable).
Precisely state the resource requirements (RAM, number of cores, CPU frequency, etc.), which you used to test your artifact. In most cases, your resource requirements should be modest and allow replication of results even on laptops. If your tool demands a more specialized resource requirement than would be appropriate for a laptop, make a note of this in your README.
* Please provide for each task/step of the replication (an estimate) how long it will take to perform it or how long it took for you and what exact machine(s) you used.
* For tasks that require a large amount of resources (hardware or time), we recommend to provide a possibility to replicate a subset of the results with reasonably modest resource and time limits, e.g., within 8 hours on a reasonable personal computer. In this case, please also include a script to replicate only a subset of the results. If this is not possible, please contact the artifact evaluation chairs early, but no later than before submission.

## Publication of Artifacts

The artifact evaluation committee uses the submitted artifact only for the artifact evaluation. It may not publicize the artifact or any parts of it during or after completing evaluation. Artifacts and all associated data will be deleted at the end of the evaluation process. We encourage the authors of artifacts to make their artifacts also permanently available, e.g., on [Zenodo](https://zenodo.org/https://figshare.com/) or [figshare](), and refer to them in their papers via a DOI. All artifacts for which a DOI exists that is known to the artifact evaluation committee are granted the availability badge.
