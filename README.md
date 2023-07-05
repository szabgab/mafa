
# Table of Contents

-   [Installation](#org2c6fa94)
    -   [Prerequisite](#orga361cc2)
    -   [Option 1: Cargo install (recommended)](#org6a274a2)
    -   [Option 2: Build from source](#org66d8512)
    -   [Option 3: Github releases](#org3e674af)
-   [Mafa is for me?](#orge67297a)
-   [What is Mafa](#orgb0958a6)
    -   [How Mafa works](#orgc16c718)
    -   [Why Mafa](#orgd6d04d7)
    -   [About Mafa](#orgc009a8d)
-   [Supported modules ](#org1d9004c)
-   [License](#org9ca5fcc)



<a id="org2c6fa94"></a>

# Installation


<a id="orga361cc2"></a>

## Prerequisite

Mafa does not work alone, below are programs that it
depends on:

1.  firefox (91 or later)

2.  curl (any version)

3.  tar (any version)

4.  gzip (any version)


<a id="org6a274a2"></a>

## Option 1: Cargo install (recommended)

This is recommended because by `cargo install`, you always get the
latest stable version of Mafa.

If you have Cargo installed, then you can

    cargo install mafa
    
    # check installed version
    mafa --version


<a id="org66d8512"></a>

## Option 2: Build from source

    # grab the source
    git clone https://github.com/imichael2e2/mafa
    
    # into source directory
    cd mafa
    
    # build
    cargo build --release --features imode,twtl,gtrans
    
    # check built version
    ./target/release/mafa --version


<a id="org3e674af"></a>

## Option 3: Github releases

&#x2026;


<a id="orge67297a"></a>

# Mafa is for me?

Mafa is for you if 

-   You believe that text is more powerful than images or videos in 
    terms of information delivery.

-   You believe that the vast majority of Web UIs are far from
    efficient, but still have faith in our Web.

-   You believe that most jobs should do in a terminal rather than
    a GUI application.

However, Mafa is **NOT** for you if

-   You want to browse websites without a web browser. (Mafa needs
    Firefox)

-   You want to see every detail of a website. (Use your favorite web 
    browser instead)

-   You plan to crawl a whole website and extract all its
    data. (A dedicated web crawler or data scraper does a better job)


<a id="orgb0958a6"></a>

# What is Mafa

Mafa is a command-line tool that helps people interact with online
websites in a terminal(tty). It accesses websites through
*modules*. Modules are child programs that rely on [WebDriver](https://www.w3.org/TR/webdriver) to do
their job. Each module has a fixed destination website and has a
specific job for that site. With modules, users can browse websites
without interacting with web browsers directly. The supported  
modules are listed [below](#org9e9789f).  


<a id="orgc16c718"></a>

## How Mafa works

Mafa leverages [WebDriver](https://www.w3.org/TR/webdriver) to achieve its goals. More specifically,
Mozilla's [GeckoDriver](https://github.com/mozilla/geckodriver) is in use. With WebDriver, Mafa
can act like a human, browsing websites naturally for its user. 


<a id="orgd6d04d7"></a>

## Why Mafa


### Usable & Convenient

Unlike other counterparts, Mafa strives to balance usability and
convenience: Mafa will try its best to finish the task on its own or
instruct users to open web browser directly if it cannot
perfectly handle the situation(such as in cases where the website
is equipped with CAPTCHA or requires user login). What Mafa tries to
be is a browser companion, **not** a replacement.


### Neutral

The underlying WebDriver backs by a nearly full-functional web
browser. Overall, Mafa default **not** to subjectively strip any feature
a website user or provider can take advantage of, just like on a
normal full-functional web browser.

Therefore there is no reason for providers to particularly prevent
Mafa from accessing their websites, which likely leads to a negative
result for **both** sides. 

It is noteworthy that Mafa does not wipe out the user identity by
default, as a regular web browser does. It is essential for website
providers because while many websites abuse user privacy, there are
always ones collecting it for a good reason, such as [Ecosia](https://www.ecosia.org).


### Stable & Long-lasting

One of Mafa's goals is to handle websites stably for a relatively long
period. Modern web pages are famous for their dynamic characteristic.
However, Mafa can handle those dynamic and unpredictable
web pages as effortlessly as the static ones. 


<a id="orgc009a8d"></a>

## About Mafa

Mafa is initially developed for (**M**)aking (**A**)PI (**F**)ree
(**A**)gain. Here "free" is the same word defined in
[What is Free Software?](https://www.gnu.org/philosophy/free-sw.en.html), i.e., as in "free speech", not as in"free
beer". Some websites provide their data *publicly* but do not
publish corresponding APIs to access it, while others offer their data
*publicly* in their carefully designed websites and APIs but with even
more carefully designed pricing. Those websites are blocking users
from accessing their *public* data by either not providing APIs or
providing ones with non-trivial barriers, examples of disrespecting
users' freedom.

Mafa is the one who fights against them and protects web users'
freedom. Because Mafa believes that as long as the data is publicly
accessible for all users without discrimination, the APIs to access it
should be as well. 


<a id="org1d9004c"></a>

# Supported modules <a id="org9e9789f"></a>

-   IMODE: Interactive mode.

-   TWTL: Twitter users' timeline.

-   GTRANS: Google translation service.


<a id="org9ca5fcc"></a>

# License

Mafa is proudly licensed under GPLv3.

See LICENSE-GPL for details.
