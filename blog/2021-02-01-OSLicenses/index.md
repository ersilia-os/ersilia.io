---
title: Open Source Licenses in EOS Initiative
slug: os-licenses
author: [gturon]
date: 2021-02-01
excerpt: "Open Source Licenses, take your pick!"
---

### Open Source Licenses in EOS Initiative

Coming from an academic background, the establishment of Ersilia Open Source Initiative as an Open Science project was the obvious way forward, but as we were not experts on copyrights, licensing and general proprietary law, some long discussions about our open source policies followed. This blogpost aims to catalyze our discussions on the matter, explaining why and what we license and hoping it might eventually help others in the same position.

First, let’s focus on the meaning of Free Open Source Software (FOSS). There are two main initiatives dedicated to promoting the use and development of FOSS,  the [Free Software Foundation](https://www.fsf.org/) (FSF) and the [Open Source Initiative](https://opensource.org/) (OSI). They both state that FOSS must be free to use, copy, distribute and modify by anyone (the ambiguity of the word Free in english is well resolved by this FSF statement *You should think of “free” as in “free speech,” not as in “free beer”*(1)), but differ in their philosophy. If you want to further deepen in the differences between movements, I have found this [article](https://opensource.com/article/17/11/open-source-or-free-software) by Scott K Peterson very clarifying. From now on in the post we will refer to our software as OSS, as we have taken the 10 principles defined by OSI as our guidelines.

Now, we can dive in the world of licenses. The most famous ones are probably Creative Commons (CC) licenses, which are usually applied to any copyrighted material, except software. You can license your software using CC, but there are some compatibility disadvantages and CC itself advises you not to. Nevertheless, knowing how CC licenses are organized is important, as most projects do not only contain software but also release other materials. For example, the content of our website, including this post, is under a Creative Commons Attribution ShareAlike 4.0 International License. CC licenses include a combination of the following restrictions (disclaimer: this is just a summary, for further reading and understanding of each type of license, please refer to [CC](https://creativecommons.org/licenses/)) :
* BY (Attribution): always give credit for the original creation to the licenser.
* SA (ShareAlike): derived work must be licensed under the same license.
* ND (NonDerivative): adapted work cannot be shared.
* NC (NonCommercial): the licensed material cannot be used for commercial purposes.
An additional CC0 license has been created to allow public content (without attribution) to be released.

Open Source Software Licenses, approved by OSI, can be divided into two categories:
Copyleft: inclusion of a ShareAlike attribute. This ensures no further restrictions will ever be placed on this software, protecting its community of users
Permissive: allow the modification and sharing of the source code under different licensing. Therefore, software released under a permissive license can be included in a closed-source software.

So, after this overview, which were Ersilia Open Source Initiative choices? As mentioned above, our contents (text, posts, documentation) are distributed under a CC BY 4.0 license, allowing visitors to use and modify them for their own benefit. The Ersilia software is released under a permissive OSS license, the  [MIT](https://opensource.org/licenses/MIT). The decision of using an MIT license instead of others with similar attributes but perhaps more common, such as the [Apache 2.0](https://opensource.org/licenses/Apache-2.0) was due to its simplicity and shortness. Importantly, the technology we use to develop our models, the Chemical Checker (2), is also released using an MIT license. We decided to not limit the use of EOSI work to noncommercial (i.e by choosing a CC-NC license, or a copyleft for software) because for the advancement of our mission, we welcome collaborations whose final purpose is not solely academic, but the development and commercialization of new drugs. It is important to remember that “free” does not mean “non commercial”. There is a growing pool of non-for-profit pharma companies, which capitalize on open source tools for drug development at affordable costs, but this topic is for another post.
Finally, we would like to remind our users that we only retain control over the software we produce. We anticipate this will affect our products in two fronts 1) Software: models by third-party authors that are incorporated in the Ersilia Platform will be limited by the licenses stated by their authors (if any). 2) Data: most data we use for model training is released in open platforms and appropriately referenced. When specific collaborations require that some data remain private, EOSI Trustee’s will decide if the usage of such data is key in our mission, and if it is the case, models will be released without making public all training sets.

(1)"What is free software? The Free Software Definition". The GNU Project -- GNU.org.
(2) Duran-Frigola et al, Nature Biotechnology, 2020
