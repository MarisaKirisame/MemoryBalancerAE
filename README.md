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

When packaging your artifact, please keep in mind: a) how accessible you are making your artifact to other researchers, and b) the fact that the AEC members will have a limited time in which to make an assessment of each artifact.

We recommend that your artifact contain a bootable virtual machine image with all of the necessary libraries installed. Using a virtual machine provides a way to make an easily reproducible environment — it is less susceptible to bit rot. It also helps the AEC have confidence that errors or other problems cannot cause harm to their machines.

Submitting source code that must be compiled is permissible. A more automated and/or portable build — such as a Docker file or a build tool that manages all compilation and dependencies (e.g., maven, gradle, etc.) — improves the odds the AEC will not be stuck getting different versions of packages working (particularly different releases of programming languages).

You should make your artifact available as a single archive file and use the naming convention <paper #>.<suffix>, where the appropriate suffix is used for the given archive format. Please use a widely available compressed archive format such as ZIP (.zip), tar and gzip (.tgz), or tar and bzip2 (.tbz2). Please use open formats for documents.

Some of the results are performance data, and therefore exact numbers depend on the particular hardware. In this case, artifacts should explain how to recognize when experiments on other hardware reproduce the high-level results (e.g., that a certain optimization exhibits a particular trend, or that comparing two tools one outperforms the other in a certain class of cases).

Common issues in the kick-the-tires phase in past years artifact evaluation included:
    Overstating platform support. Several artifacts claiming the need for only UNIX-like systems failed severely under macOS — in particular those requiring 32-bit compilers, which are no longer present in newer macOS versions. We recommend future artifacts scope their claimed support more narrowly. Generally this could be fixed by the authors providing a Dockerfile.
    Missing dependencies, or poor documentation of dependencies.
    As with last year, the single most effective way to avoid these sorts of issues ahead of time is to run the instructions independently on a fresh machine, VM, or Docker container.

Common issues found during past years full review phase included:
    Not explaining how to interpret results. Several artifacts ran successfully and produced the output that was the basis for the paper, but without any way for reviewers to compare these for consistency with the paper. Examples included generating a list of warnings without documenting which were true vs. false positives, and generating large tables of numbers that were presented graphically in the paper without providing a way to generate analogous visualizations.
