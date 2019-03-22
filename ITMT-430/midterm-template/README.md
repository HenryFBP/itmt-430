
# Midterm Report

## ITMT 430 2019 - Henry Post

### Sprint 01: Developer

#### Create comprehensive Git guide for all members

https://github.com/illinoistech-itm/2019-team-07f/blob/master/Reports/documents/How%20to%20contribute%20to%20this%20project.pdf

#### Created Python library to convert MP4 to MP3

- It works multithreaded
- Documented all work in README and in Trello

  [Link to current
  README.md](https://github.com/illinoistech-itm/2019-team-07f/blob/master/tools/video-to-audio/report.md)

  ![Proof that I documented my work about the V2AServer in
  Trello.](v2aserver-proof.PNG)
    
- Test cases and unit tests
- Built, installed, and tested each time `vagrant up` is run
- Works with Java via a library called `jep`, included in unit tests.
  
  
##### First version:  

https://github.com/illinoistech-itm/2019-team-07f/commit/a5b718e6a07ecc42976d37b6320b47d3713a46b7

##### Final version with test cases:  

https://github.com/illinoistech-itm/2019-team-07f/commit/e9c9777b69dcdc271cd5636767bdf44ee21a022e

##### Vagrantfile to test my library:  

https://github.com/illinoistech-itm/2019-team-07f/commit/09b815f907fb84bf3fec5fe27648e92dc6f9c33f

##### Set up Java support for my Python library:

https://github.com/illinoistech-itm/2019-team-07f/commit/3ab18f6489099a3fd07b747df731f9de9f25f872

##### Documenting my V2AServer:

https://github.com/illinoistech-itm/2019-team-07f/commit/bbcc6b5132c1e589c07cce623d159023b64849fe

#### Populated the README with all member contact information

The PM should have done this step, but it was unfinished for so long that I just
had to.

https://github.com/illinoistech-itm/2019-team-07f/commit/bdfa806657cfffdc50bf0936805a28b72115b34e


#### Created skeletal Apache Tomcat Servlet

##### Creating the server and all documentation

https://github.com/illinoistech-itm/2019-team-07f/commit/1f2b946e63cea66a4c3aea5c40938ffb3129d5a2

##### Making a Vagrantfile section that compiles and deploys the servlet

https://github.com/illinoistech-itm/2019-team-07f/commit/4812f0ae75425e4a99f3f3bbd81b399066a69417

### Sprint 02: IT Operation

#### Making cross-IDE documentation for editing the Java Servlet 

https://github.com/illinoistech-itm/2019-team-07f/commit/78730703e2d291376f938154c1d541393b825b49

#### Adding Hibernate (ORM framework) to the project

https://github.com/illinoistech-itm/2019-team-07f/commit/45f154f5c85617fc8e0d69290406c61105a16386

#### Add MySQL to Vagrantfile

![Proof that I documented my work about MySQL setup in the Vagrantfile in
Trello.](mysql-proof.PNG)

https://github.com/illinoistech-itm/2019-team-07f/commit/d434693d0e974f8632e1bd8e5c605a86629e07ce


#### Begin setting up packer

##### Initial packer json file

https://github.com/illinoistech-itm/2019-team-07f/commit/b5bdad221bc797727a1cdd71119750d3c08e9626

##### Document and further set up packer json file

https://github.com/illinoistech-itm/2019-team-07f/commit/b5bdad221bc797727a1cdd71119750d3c08e9626

##### Extract shell scripts from packer to Vagrantfile

https://github.com/illinoistech-itm/2019-team-07f/commit/0f937356e5d2bf13c84a092f5aa0578666d15429

### Sprint 03: UI/UX

#### Fix broken HTML and CSS for designers

https://github.com/illinoistech-itm/2019-team-07f/commit/3df795d70e8ac77d8a11a477090ca7e1fe3f8d83

![Proof that I documented my work about the broken CSS in
Trello.](fix-broken-css-proof.PNG)

##### Re-do and simplify much of HTML/CSS

I took a 500-line CSS file down to about 20 lines. I also fixed many, many, many
spelling and HTML errors.

https://github.com/illinoistech-itm/2019-team-07f/commit/856d67a1c86793e760db6681d14e3bd1bbf66d46

https://github.com/illinoistech-itm/2019-team-07f/commit/53ff14f60d7e1b380d0c043d09458db984f81c90

![Proof that I documented my work about re-doing the messy HTML+CSS in
Trello.](redo-html-proof.PNG)

#### Add test users to Vagrant provisioning step

https://github.com/illinoistech-itm/2019-team-07f/commit/d7b4c5e471637dfbec0d1dbe954020ae7439f898

#### Use SSH keys to clone git repo

![Proof that I documented my work about the GitHub deploy keys in
Trello.](use-github-ssh-keys-proof.PNG)

https://github.com/illinoistech-itm/2019-team-07f/commit/bb55dfc6dd4f7d94f3f7206bbba84d104d65c9a9

https://github.com/illinoistech-itm/2019-team-07f/commit/e031995b25cf7d94ed6eea274a573df5c33edb85

https://github.com/illinoistech-itm/2019-team-07f/commit/6d8cfbc79dedb0d9e029c9a7724e80a0e6697584

#### Fully separate MySQL box from Web box

![Proof that I documented my work about separating vagrant boxes in
Trello.](separate-vagrant-boxes-proof.PNG)

https://github.com/illinoistech-itm/2019-team-07f/commit/b66ca06421a725ce0bbbb0c8fc206e63c412cdb0

https://github.com/illinoistech-itm/2019-team-07f/commit/53772dea9cbc81ee55853a876a47ff3cec86630f

https://github.com/illinoistech-itm/2019-team-07f/commit/44a1fa6a1a1bec58cfeae5460868ed0c11462ddf
