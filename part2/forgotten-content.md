# Forgotten content

The challenges in this chapter are all about files that were either
forgotten, accidentally misplaced or have been added as a joke by the
development team.

## Challenges covered in this chapter

| Challenge                                                                          | Difficulty |
|:-----------------------------------------------------------------------------------|:-----------|
| Let us redirect you to a donation site that went out of business.                  | 1 of 5     |
| Access a confidential document.                                                    | 1 of 5     |
| Use a deprecated B2B interface that was not properly shut down.                    | 1 of 5     |
| Access a salesman's forgotten backup file.                                         | 2 of 5     |
| Access a developer's forgotten backup file.                                        | 3 of 5     |
| Find the hidden easter egg.                                                        | 3 of 5     |
| Travel back in time to the golden era of web design.                               | 3 of 5     |
| Deprive the shop of earnings by downloading the blueprint for one of its products. | 3 of 5     |
| Access a misplaced SIEM signature file.                                            | 3 of 5     |
| Retrieve the language file that never made it into production.                     | 5 of 5     |

### Let us redirect you to a donation site that went out of business

One of the sites that the Juice Shop accepted donations from went out of
business end of 2017.

#### Hints

* When removing references to the site from the code the developers have
  been a bit sloppy.
* It is of course not sufficient to just visit the donation site
  _directly_ to solve the challenge.

### Access a confidential document

Somewhere in the application you can find a file that contains sensitive
information about some - potentially hostile - takeovers the Juice Shop
top management has planned.

#### Hints

* Analyze and tamper with links in the application that deliver a file
  directly.
* The file you are looking for is not protected in any way. Once you
  _found it_ you can also _access it_.

### Use a deprecated B2B interface that was not properly shut down

The Juice Shop represents a classic Business-to-Consumer (B2C)
application, but it also has some enterprise customers for which it
would be inconvenient to order large quantities of juice through the
webshop UI. For those customers there is a dedicated B2B interface.

#### Hints

* The old B2B interface was replaced with a more modern version
  recently.
* When deprecating the old interface, not all of its parts were cleanly
  removed from the code base.
* Simply using the deprecated interface suffices to solve this
  challenge. No attack or exploit is necessary.

### Access a salesman's forgotten backup file

A sales person as accidentally uploaded a list of (by now outdated)
coupon codes to the application. Downloading this file will not only
solve the _Access a salesman's forgotten backup file_ challenge but
might also prove useful in another challenge later on.

#### Hints

* Analyze and tamper with links in the application that deliver a file
  directly.
* The file is not directly accessible because a security mechanism
  prevents access to it.
* You need to trick the security mechanism into thinking that the file
  has a valid file type.
* For this challenge there are _two approaches_ to pull this trick.

### Access a developer's forgotten backup file

During an emergency incident and the hotfix that followed, a developer
accidentally pasted an application configuration file into the wrong
place. Downloading this file will not only solve the _Access a
developer's forgotten backup file_ challenge but might also prove
crucial in several other challenges later on.

#### Hints

* Analyze and tamper with links in the application that deliver a file
  directly.
* The file is not directly accessible because a security mechanism
  prevents access to it.
* You need to trick the security mechanism into thinking that the file
  has a valid file type.
* For this challenge there is only _one approach_ to pull this trick.

### Find the hidden easter egg

> An Easter egg is an intentional inside joke, hidden message, or
> feature in an interactive work such as a computer program, video game
> or DVD menu screen. The name is used to evoke the idea of a
> traditional Easter egg hunt.[^1]

#### Hints

* If you solved one of the other four file access challenges, you
  already know where the easter egg is located
* Simply reuse the trick that already worked for the files above

_When you open the easter egg file, you might be a little disappointed,
as the developers taunt you about not having found **the real** easter
egg! Of course finding **that** is
[a follow-up challenge](crypto.md#apply-some-advanced-cryptanalysis-to-find-the-real-easter-egg)
to this one._

### Travel back in time to the golden era of web design

You probably agree that this is one of the more ominously described
challenges. But the description contains a very obvious hint what this
whole _time travel_ is about.

#### Hints

![Time travel challenge on the score board](img/travel-back-in-time_challenge.png)

* The mentioned _golden era_ lasted from 1994 to 2009.
* You can solve this challenge by requesting a specific file

_While requesting a file is sufficient to solve this challenge, you
might want to invest a little bit of extra time for the **full
experience** where you actually put the file **in action** with some DOM
tree manipulation! Unfortunately the nostalgic vision only lasts until
the next time you hit `F5` in your browser._

### Deprive the shop of earnings by downloading the blueprint for one of its products

Why waste money for a product when you can just as well get your hands
on its blueprint in order to make it yourself?

#### Hints

* The product you might want to give a closer look is the _OWASP Juice
  Shop Logo (3D-printed)_
* For your inconvenience the blueprint was _not_ misplaced into the same
  place like so many others forgotten files covered in this chapter

:information_source: _If you are running the Juice Shop with a custom
theme and product inventory, the product to inspect will be a different
one. The tooltip on the Score Board will tell you which one._

### Access a misplaced SIEM signature file.

> Security information and event management (SIEM) technology supports
> threat detection and security incident response through the real-time
> collection and historical analysis of security events from a wide
> variety of event and contextual data sources. It also supports
> compliance reporting and incident investigation through analysis of
> historical data from these sources. The core capabilities of SIEM
> technology are a broad scope of event collection and the ability to
> correlate and analyze events across disparate sources.[^2]

The misplaced signature file is actually a rule file for
[Sigma](https://github.com/Neo23x0/sigma), a generic signature format
for SIEM systems:

> Sigma is a generic and open signature format that allows you to
> describe relevant log events in a straight forward manner. The rule
> format is very flexible, easy to write and applicable to any type of
> log file. The main purpose of this project is to provide a structured
> form in which researchers or analysts can describe their once
> developed detection methods and make them shareable with others.
>
> Sigma is for log files what Snort is for network traffic and YARA is
> for files.[^3]

#### Hints

* If you solved one of the other four file access challenges, you
  already know where the SIEM signature file is located
* Simply reuse the trick that already worked for the files above

### Retrieve the language file that never made it into production

> A project is internationalized when all of the project’s materials and
> deliverables are consumable by an international audience. This can
> involve translation of materials into different languages, and the
> distribution of project deliverables into different countries.[^4]

Following this requirement OWASP sets for all its projects, the Juice
Shop's user interface is available in different languages. One extra
language is actually available that you will not find in the selection
menu.

![Language selection dropdown](/part3/img/languages.png)

#### Hints

* First you should find out how the languages are technically changed in
  the user interface.
* Guessing will most definitely not work in this challenge.
* You should rather choose between the following two ways to beat this
  challenge:
  * _Apply brute force_ (and don't give up to quickly) to find it.
  * _Investigate externally_ what languages are actually available.

[^1]: https://en.wikipedia.org/wiki/Easter_egg_(media)

[^2]: https://www.gartner.com/it-glossary/security-information-and-event-management-siem/

[^3]: https://github.com/Neo23x0/sigma#what-is-sigma

[^4]: https://www.owasp.org/index.php/OWASP_2014_Project_Handbook#tab=Project_Requirements

