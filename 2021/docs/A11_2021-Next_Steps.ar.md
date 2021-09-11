# A11:2021 – Next Steps
Organizations working towards a mature appsec program or security
consultancies or tool vendors wishing to expand coverage for their
offerings, the following four issues are well worth the effort to
identify and remediate.

## Code Quality issues

| CWEs Mapped  | Max Incidence Rate  | Avg Incidence Rate  | Max Coverage  | Avg Coverage  | Avg Weighted Exploit  | Avg Weighted Impact  | Total Occurrences  | Total CVEs  |
|:-------------:|:--------------------:|:--------------------:|:--------------:|:--------------:|:----------------------:|:---------------------:|:-------------------:|:------------:|
| 38           | 49.46%              | 2.22%               | 60.85%        | 23.42%        |                       |                      | 101736             | 7564        |

-   **Description.** Code quality issues include known security defects
    or patterns, reusing variables for multiple purposes, exposure of
    sensitive information in debugging output, off-by-one errors, time
    of check/time of use (TOCTOU) race conditions, unsigned or signed
    conversion errors, use after free, and more. The hallmark of this
    section is that they can usually be identified with stringent
    compiler flags, static code analysis tools, and linter IDE plugins.
    Modern languages by design eliminated many of these issues, such as
    Rust’s memory ownership and borrowing concept, Rust’s threading
    design, and Go’s strict typing and bounds checking.

-   **How to prevent**. Enable and use your editor and language’s static
    code analysis options. Consider using a static code analysis tool.
    Consider if it might be possible to use or migrate to a language or
    framework that eliminates bug classes, such as Rust or Go.

-   **Example attack scenarios**. An attacker might obtain or update
    sensitive information by exploiting a race condition using a
    statically shared variable across multiple threads.

-   **References**. TBA

## Denial of Service

| CWEs Mapped  | Max Incidence Rate  | Avg Incidence Rate  | Max Coverage  | Avg Coverage  | Avg Weighted Exploit  | Avg Weighted Impact  | Total Occurrences  | Total CVEs  |
|:-------------:|:--------------------:|:--------------------:|:--------------:|:--------------:|:----------------------:|:---------------------:|:-------------------:|:------------:|
| 8            | 17.54%              | 4.89%               | 79.58%        | 33.26%        |                       |                      | 66985              | 973         |

-   **Description**. Denial of service is always possible given
    sufficient resources. However, design and coding practices have a
    significant bearing on the magnitude of the denial of service.
    Suppose anyone with the link can access a large file, or a
    computationally expensive transaction occurs on every page. In that
    case, denial of service requires less effort to conduct.

-   **How to prevent**. Performance test code for CPU, I/O, and memory
    usage, re-architect, optimize, or cache expensive operations.
    Consider access controls for larger objects to ensure that only
    authorized individuals can access huge files or objects or serve
    them by an edge caching network.

-   **Example attack scenarios**. An attacker might determine that an
    operation takes 5-10 seconds to complete. When running four
    concurrent threads, the server seems to stop responding. The
    attacker uses 1000 threads and takes the entire system offline.

-   **References**. TBA

## Memory Management Errors

| CWEs Mapped  | Max Incidence Rate  | Avg Incidence Rate  | Max Coverage  | Avg Coverage  | Avg Weighted Exploit  | Avg Weighted Impact  | Total Occurrences  | Total CVEs  |
|:-------------:|:--------------------:|:--------------------:|:--------------:|:--------------:|:----------------------:|:---------------------:|:-------------------:|:------------:|
| 14           | 7.03%               | 1.16%               | 56.06%        | 31.74%        |                       |                      | 26576              | 16184       |

-   **Description**. Web applications tend to be written in managed
    memory languages, such as Java, .NET, or node.js (JavaScript or
    TypeScript). However, these languages are written in systems
    languages that have memory management issues, such as buffer or heap
    overflows, use after free, integer overflows, and more. There have
    been many sandbox escapes over the years that prove that just
    because the web application language is nominally memory “safe,” the
    foundations are not.

-   **How to prevent**. Many modern APIs are now written in memory-safe
    languages such as Rust or Go. In the case of Rust, memory safety is
    a crucial feature of the language. For existing code, the use of
    strict compiler flags, strong typing, static code analysis, and fuzz
    testing can be beneficial in identifying memory leaks, memory, and
    array overruns, and more.

-   **Example attack scenarios**. Buffer and heap overflows have been a
    mainstay of

-   **References**. TBA

## Security Control Failures

| CWEs Mapped  | Max Incidence Rate  | Avg Incidence Rate  | Max Coverage  | Avg Coverage  | Avg Weighted Exploit  | Avg Weighted Impact  | Total Occurrences  | Total CVEs  |
|:-------------:|:--------------------:|:--------------------:|:--------------:|:--------------:|:----------------------:|:---------------------:|:-------------------:|:------------:|
| 2            | 11.35%              | 9.64%               | 76.60%        | 45.23%        |                       |                      | 44911              | 329         |

-   **Description**.

-   **How to prevent**.

-   **Example attack scenarios**.

-   **References**. TBA
