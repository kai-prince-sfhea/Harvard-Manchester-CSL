# Attribution and rights status

## Starting CSL

The imported style is credited to the Library Student Team at the University of
Manchester: Adrian Kosikowski (author), with Lea Anderton, David Hirst, Dhruv
Mistry and Preenal Asher (contributors). Their CSL metadata roles are retained.
Kai Prince's subsequent maintenance is recorded in Git history and the README.

Kai Prince has confirmed written permission to develop this CSL and directed
that the [University copyright notice](COPYRIGHT.md) be applied. The current
candidate carries that notice in both its documentation and CSL rights metadata.
It asserts no Apache, Creative Commons or general public reuse licence.

The [initial public import](https://github.com/kai-prince-sfhea/Harvard-Manchester-CSL/tree/4f9b12d9cda7a4098b30a78e150c47e378e6d20c)
and starting CSL had no explicit licence or rights element. Their public
availability and Zotero-shaped identifier do not establish additional rights.
The private permission correspondence is not distributed with this candidate.

## Library guidance and historical material

The [University Library guide](https://subjects.library.manchester.ac.uk/referencing/harvard)
informs the style rules. The Library is not claimed to endorse this candidate.
The Harvard guide pages link to the University's reserved-rights notice; no
open licence was found on those pages or in their linked PDF. A Creative Commons
notice on the separate APA page is not presented as a licence for Harvard.
The current payload does not include the guide PDF, its historical example
library or the generated website/cache. The maintained starter records are
fictional; their placeholder URLs/DOI are not source evidence.

Existing repository history still contains the earlier guide-derived material
and generated Quarto assets, including third-party browser libraries and fonts.
Removing them from the current tree does not remove that history. The scoped
historical appendix below supplies known component attributions and licence
texts prospectively. It does not rewrite old commits, establish earlier notice
compliance or settle every historical item's rights. Those component terms do
not relicense the current CSL or the University material.

## Current dependencies

Only the `.csl` file is needed to use the style. The current user payload bundles
no browser libraries, fonts, AI models, schemas or test processors. Quarto,
Pandoc, citeproc-js, validation schemas and other developer tools are separate
software under their own terms, outside this payload.

## Historical generated-output notices

This appendix applies only to the 16 browser-library, font and output-support
assets retained under `_site/site_libs/` in the existing five-commit Git history,
from `4f9b12d9cda7a4098b30a78e150c47e378e6d20c` through
`1b72d62dffa2f628d53c23e6bb8ca8f7a7256cb8`. These assets are absent from the
current source snapshot and are not needed to use the downloadable CSL.

Their original bytes and embedded notices remain unchanged in history. The
known historical terms below are separate from the [University copyright
notice](COPYRIGHT.md). No Apache or MIT licence is granted for the CSL, the
Library guide, bibliography examples, private correspondence or unrelated
contributors' material by this appendix. Preserve this appendix when copying
the repository together with its historical assets.

The matched Quarto output-support resources correspond to the official Quarto
`v1.7.34` resource files; this does not identify the executable that generated
the original website. Compiled Bootstrap styling and the Icons font retain
their component terms. Dependency notices below cover the Clipboard and
Autocomplete bundles as well as their declared runtime components. Tagged
package/lock provenance identifies those dependency versions; the embedded
modules were not separately de-minified or individually byte-compared.

### Historical MIT components and full terms

```text
Quarto output support JavaScript and related resources
Copyright (c) 2020-2024 Posit Software, PBC
https://github.com/quarto-dev/quarto-cli/blob/v1.7.34/COPYRIGHT

Bootstrap 5.3.1
Copyright (c) 2011-2023 The Bootstrap Authors
https://github.com/twbs/bootstrap/blob/v5.3.1/LICENSE

Bootstrap Icons 1.11.1 (including the font)
Copyright (c) 2019-2023 The Bootstrap Authors
https://github.com/twbs/icons/blob/v1.11.1/LICENSE

clipboard.js 2.0.11; good-listener 1.2.2; select 1.1.2; delegate 3.2.0
Copyright (c) Zeno Rocha
https://github.com/zenorocha/clipboard.js/blob/v2.0.11/LICENSE
https://github.com/zenorocha/good-listener/blob/v1.2.2/readme.md
https://github.com/zenorocha/select/blob/v1.1.2/readme.md
https://github.com/zenorocha/delegate/blob/v3.2.0/readme.md

tiny-emitter 2.1.0 (within the Clipboard bundle)
Copyright (c) 2017 Scott Corgan
https://github.com/scottcorgan/tiny-emitter/blob/2.1.0/LICENSE

AnchorJS 5.0.0
Copyright (c) 2021 Bryan Braun (upstream LICENSE)
Copyright (c) 2023 Bryan Braun (historical bundle header)
https://github.com/bryanbraun/anchorjs/blob/5.0.0/LICENSE

Popper 2.11.7
Copyright (c) 2019 Federico Zivolo
https://github.com/floating-ui/floating-ui/blob/v2.11.7/LICENSE.md

Tippy 6.3.7
Copyright (c) 2017-present atomiks
https://github.com/atomiks/tippyjs/blob/v6.3.7/LICENSE

Algolia Autocomplete JS 1.11.1 and its Algolia packages
Copyright (c) 2015-present Algolia, Inc.
Historical bundle attribution: Algolia, Inc. and contributors
https://github.com/algolia/autocomplete/blob/v1.11.1/LICENSE

Preact 10.13.2 (within the Autocomplete bundle)
Copyright (c) 2015-present Jason Miller
https://github.com/preactjs/preact/blob/10.13.2/LICENSE

The following MIT permission and warranty terms apply to the MIT components
identified above, retaining their respective copyright notices:

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

### Historical Apache 2.0 components

```text
Fuse.js 6.6.2
Copyright 2017 Kirollos Risk (upstream LICENSE)
Copyright (c) 2022 Kiro Risk (historical bundle header)
https://github.com/krisk/Fuse/blob/v6.6.2/LICENSE

htm 3.1.1 (within the Autocomplete bundle)
Copyright 2018 Google Inc.
https://github.com/developit/htm/blob/3.1.1/LICENSE
```

The following full Apache License, Version 2.0 applies to those historical
Apache components. It is reproduced unchanged for that purpose; it is not the
licence for the current CSL or a replacement for COPYRIGHT.md. The checked
Fuse 6.6.2 and htm 3.1.1 tagged distributions contained no separate NOTICE file
beyond their checked licences; no additional NOTICE attribution is invented.

```text

                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
      outstanding shares, or (iii) beneficial ownership of such entity.

      "You" (or "Your") shall mean an individual or Legal Entity
      exercising permissions granted by this License.

      "Source" form shall mean the preferred form for making modifications,
      including but not limited to software source code, documentation
      source, and configuration files.

      "Object" form shall mean any form resulting from mechanical
      transformation or translation of a Source form, including but
      not limited to compiled object code, generated documentation,
      and conversions to other media types.

      "Work" shall mean the work of authorship, whether in Source or
      Object form, made available under the License, as indicated by a
      copyright notice that is included in or attached to the work
      (an example is provided in the Appendix below).

      "Derivative Works" shall mean any work, whether in Source or Object
      form, that is based on (or derived from) the Work and for which the
      editorial revisions, annotations, elaborations, or other modifications
      represent, as a whole, an original work of authorship. For the purposes
      of this License, Derivative Works shall not include works that remain
      separable from, or merely link (or bind by name) to the interfaces of,
      the Work and Derivative Works thereof.

      "Contribution" shall mean any work of authorship, including
      the original version of the Work and any modifications or additions
      to that Work or Derivative Works thereof, that is intentionally
      submitted to Licensor for inclusion in the Work by the copyright owner
      or by an individual or Legal Entity authorized to submit on behalf of
      the copyright owner. For the purposes of this definition, "submitted"
      means any form of electronic, verbal, or written communication sent
      to the Licensor or its representatives, including but not limited to
      communication on electronic mailing lists, source code control systems,
      and issue tracking systems that are managed by, or on behalf of, the
      Licensor for the purpose of discussing and improving the Work, but
      excluding communication that is conspicuously marked or otherwise
      designated in writing by the copyright owner as "Not a Contribution."

      "Contributor" shall mean Licensor and any individual or Legal Entity
      on behalf of whom a Contribution has been received by Licensor and
      subsequently incorporated within the Work.

   2. Grant of Copyright License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      copyright license to reproduce, prepare Derivative Works of,
      publicly display, publicly perform, sublicense, and distribute the
      Work and such Derivative Works in Source or Object form.

   3. Grant of Patent License. Subject to the terms and conditions of
      this License, each Contributor hereby grants to You a perpetual,
      worldwide, non-exclusive, no-charge, royalty-free, irrevocable
      (except as stated in this section) patent license to make, have made,
      use, offer to sell, sell, import, and otherwise transfer the Work,
      where such license applies only to those patent claims licensable
      by such Contributor that are necessarily infringed by their
      Contribution(s) alone or by combination of their Contribution(s)
      with the Work to which such Contribution(s) was submitted. If You
      institute patent litigation against any entity (including a
      cross-claim or counterclaim in a lawsuit) alleging that the Work
      or a Contribution incorporated within the Work constitutes direct
      or contributory patent infringement, then any patent licenses
      granted to You under this License for that Work shall terminate
      as of the date such litigation is filed.

   4. Redistribution. You may reproduce and distribute copies of the
      Work or Derivative Works thereof in any medium, with or without
      modifications, and in Source or Object form, provided that You
      meet the following conditions:

      (a) You must give any other recipients of the Work or
          Derivative Works a copy of this License; and

      (b) You must cause any modified files to carry prominent notices
          stating that You changed the files; and

      (c) You must retain, in the Source form of any Derivative Works
          that You distribute, all copyright, patent, trademark, and
          attribution notices from the Source form of the Work,
          excluding those notices that do not pertain to any part of
          the Derivative Works; and

      (d) If the Work includes a "NOTICE" text file as part of its
          distribution, then any Derivative Works that You distribute must
          include a readable copy of the attribution notices contained
          within such NOTICE file, excluding those notices that do not
          pertain to any part of the Derivative Works, in at least one
          of the following places: within a NOTICE text file distributed
          as part of the Derivative Works; within the Source form or
          documentation, if provided along with the Derivative Works; or,
          within a display generated by the Derivative Works, if and
          wherever such third-party notices normally appear. The contents
          of the NOTICE file are for informational purposes only and
          do not modify the License. You may add Your own attribution
          notices within Derivative Works that You distribute, alongside
          or as an addendum to the NOTICE text from the Work, provided
          that such additional attribution notices cannot be construed
          as modifying the License.

      You may add Your own copyright statement to Your modifications and
      may provide additional or different license terms and conditions
      for use, reproduction, or distribution of Your modifications, or
      for any such Derivative Works as a whole, provided Your use,
      reproduction, and distribution of the Work otherwise complies with
      the conditions stated in this License.

   5. Submission of Contributions. Unless You explicitly state otherwise,
      any Contribution intentionally submitted for inclusion in the Work
      by You to the Licensor shall be under the terms and conditions of
      this License, without any additional terms or conditions.
      Notwithstanding the above, nothing herein shall supersede or modify
      the terms of any separate license agreement you may have executed
      with Licensor regarding such Contributions.

   6. Trademarks. This License does not grant permission to use the trade
      names, trademarks, service marks, or product names of the Licensor,
      except as required for reasonable and customary use in describing the
      origin of the Work and reproducing the content of the NOTICE file.

   7. Disclaimer of Warranty. Unless required by applicable law or
      agreed to in writing, Licensor provides the Work (and each
      Contributor provides its Contributions) on an "AS IS" BASIS,
      WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
      implied, including, without limitation, any warranties or conditions
      of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
      PARTICULAR PURPOSE. You are solely responsible for determining the
      appropriateness of using or redistributing the Work and assume any
      risks associated with Your exercise of permissions under this License.

   8. Limitation of Liability. In no event and under no legal theory,
      whether in tort (including negligence), contract, or otherwise,
      unless required by applicable law (such as deliberate and grossly
      negligent acts) or agreed to in writing, shall any Contributor be
      liable to You for damages, including any direct, indirect, special,
      incidental, or consequential damages of any character arising as a
      result of this License or out of the use or inability to use the
      Work (including but not limited to damages for loss of goodwill,
      work stoppage, computer failure or malfunction, or any and all
      other commercial damages or losses), even if such Contributor
      has been advised of the possibility of such damages.

   9. Accepting Warranty or Additional Liability. While redistributing
      the Work or Derivative Works thereof, You may choose to offer,
      and charge a fee for, acceptance of support, warranty, indemnity,
      or other liability obligations and/or rights consistent with this
      License. However, in accepting such obligations, You may act only
      on Your own behalf and on Your sole responsibility, not on behalf
      of any other Contributor, and only if You agree to indemnify,
      defend, and hold each Contributor harmless for any liability
      incurred by, or claims asserted against, such Contributor by reason
      of your accepting any such warranty or additional liability.

   END OF TERMS AND CONDITIONS

   APPENDIX: How to apply the Apache License to your work.

      To apply the Apache License to your work, attach the following
      boilerplate notice, with the fields enclosed by brackets "[]"
      replaced with your own identifying information. (Don't include
      the brackets!)  The text should be enclosed in the appropriate
      comment syntax for the file format. We also recommend that a
      file or class name and description of purpose be included on the
      same "printed page" as the copyright notice for easier
      identification within third-party archives.

   Copyright [yyyy] [name of copyright owner]

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

These attribution notices are informational and do not modify any licence.
