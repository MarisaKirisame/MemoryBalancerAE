# MemoryBalancerAE
Artifact Eval for MemoryBalancer

Artifacts should be:
    consistent with the paper,
    as complete as possible,
    well documented, and
    easy to reuse, facilitating further research.

Your submission should consist of three pieces:
    an overview of your artifact,
    a URL pointing to either:
        a single file containing the artifact (recommended), or
        the address of a public source control repository
    A hash certifying the version of the artifact at submission time: either
        an md5 hash of the single file (use the md5 or md5sum command-line tool to generate the hash), or
        the full commit hash for the repository (e.g., from git reflog --no-abbrev)

The URL must be a Google Drive, Dropbox, Github, Bitbucket, or (public) Gitlab URL, to help protect the anonymity of the reviewers. You may upload your artifact directly if it is a single file less than 15 MB.

Your overview should consist of two parts:
    a Getting Started Guide and
    Step-by-Step Instructions for how you propose to evaluate your artifact (with appropriate connections to the relevant sections of your paper);

The Getting Started Guide should contain setup instructions (including, for example, a pointer to the VM player software, its version, passwords if needed, etc.) and basic testing of your artifact that you expect a reviewer to be able to complete in 30 minutes. Reviewers will follow all the steps in the guide during an initial kick-the-tires phase. The Getting Started Guide should be as simple as possible, and yet it should stress the key elements of your artifact. Anyone who has followed the Getting Started Guide should have no technical difficulties with the rest of your artifact.

The Step by Step Instructions explain how to reproduce any experiments or other activities that support the conclusions in your paper. Write this for readers who have a deep interest in your work and are studying it to improve it or compare against it. If your artifact runs for more than a few minutes, point this out, note how long it is expected to run (roughly) and explain how to run it on smaller inputs. Reviewers may choose to run on smaller inputs or larger inputs depending on available hardware.

Where appropriate, include descriptions of and links to files (included in the archive) that represent expected outputs (e.g., the log files expected to be generated by your tool on the given inputs); if there are warnings that are safe to be ignored, explain which ones they are.

The artifact’s documentation should include the following:
    A list of claims from the paper supported by the artifact, and how/why.
    A list of claims from the paper not supported by the artifact, and why not.

Artifact reviewers can use this documentation to center their reviews / evaluation around these specific claims, though the reviewers will still consider whether the provided evidence is adequate to support claims that the artifact works.

When packaging your artifact, please keep in mind: a) how accessible you are making your artifact to other researchers, and b) the fact that the AEC members will have a limited time in which to make an assessment of each artifact.

We recommend that your artifact contain a bootable virtual machine image with all of the necessary libraries installed. Using a virtual machine provides a way to make an easily reproducible environment — it is less susceptible to bit rot. It also helps the AEC have confidence that errors or other problems cannot cause harm to their machines.

Submitting source code that must be compiled is permissible. A more automated and/or portable build — such as a Docker file or a build tool that manages all compilation and dependencies (e.g., maven, gradle, etc.) — improves the odds the AEC will not be stuck getting different versions of packages working (particularly different releases of programming languages).

You should make your artifact available as a single archive file and use the naming convention <paper #>.<suffix>, where the appropriate suffix is used for the given archive format. Please use a widely available compressed archive format such as ZIP (.zip), tar and gzip (.tgz), or tar and bzip2 (.tbz2). Please use open formats for documents.

Some of the results are performance data, and therefore exact numbers depend on the particular hardware. In this case, artifacts should explain how to recognize when experiments on other hardware reproduce the high-level results (e.g., that a certain optimization exhibits a particular trend, or that comparing two tools one outperforms the other in a certain class of cases).

Artifacts given the Functional or Reusable badge are generally referred to as accepted.

Common issues in the kick-the-tires phase in past years artifact evaluation included:
    Overstating platform support. Several artifacts claiming the need for only UNIX-like systems failed severely under macOS — in particular those requiring 32-bit compilers, which are no longer present in newer macOS versions. We recommend future artifacts scope their claimed support more narrowly. Generally this could be fixed by the authors providing a Dockerfile.
    Missing dependencies, or poor documentation of dependencies.
    As with last year, the single most effective way to avoid these sorts of issues ahead of time is to run the instructions independently on a fresh machine, VM, or Docker container.

Common issues found during past years full review phase included:
    Not explaining how to interpret results. Several artifacts ran successfully and produced the output that was the basis for the paper, but without any way for reviewers to compare these for consistency with the paper. Examples included generating a list of warnings without documenting which were true vs. false positives, and generating large tables of numbers that were presented graphically in the paper without providing a way to generate analogous visualizations.
