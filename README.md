<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://guacamole.apache.org/doc/1.5.5/gug/">
    <img src="https://www.bujarra.com/wp-content/uploads/2020/11/Apache-Guacamole-00.jpg" alt="Logo" width="913" height="536" >
  </a>

<h3 align="center">Apache Guacamole</h3>

  <p align="center">
    <br />
    <a href="https://guacamole.apache.org/doc/1.5.5/gug/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/dacapo59/guacamole">View Demo</a>
    ·
    <a href="https://github.com/dacapo59/guacamole/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    ·
    <a href="https://github.com/dacapo59/guacamole/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<!-- [![Product Name0 Screen Shot][product-screenshot]](https://example.com) -->

This document provides a guide for setting up Keycloak to enable Single Sign-On (SSO) within your organization. It outlines the steps required to configure Keycloak as your centralized identity provider, allowing users to authenticate once and gain access to multiple applications and services seamlessly. The guide covers the installation and initial configuration of Keycloak, the creation and management of realms, the integration of client applications with SSO capabilities, and the setup of authentication protocols such as OAuth 2.0 and OpenID Connect. By following this document, you will establish a robust SSO environment that enhances user convenience and security across your network.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

* [![Guacamole][guacamole-image]][guacamole-url]
* [![Tomcat][tomcat-image]][tomcat-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get started with installing Keycloak, first ensure you have administrative access to your server. Keycloak is an open-source identity and access management solution that provides comprehensive authentication and authorization capabilities. In a typical Keycloak setup, you deploy a Keycloak server that acts as a centralized identity provider, managing user identities, roles, and permissions. Keycloak supports various authentication protocols such as OAuth 2.0, OpenID Connect, and SAML, allowing seamless integration with diverse applications and services. Administrators can configure realms to manage different sets of users and applications, set up client applications with specific security settings, and establish federated identity providers to synchronize with existing identity systems. Additionally, Keycloak provides features like single sign-on (SSO), multi-factor authentication (MFA), and user federation, streamlining user management and enhancing security across your ecosystem.

### Prerequisites

* Debian OS Installed
* Download Apache Guacamole server source code
  ```sh
  cd /opt
  wget https://guacamole.apache.org/releases/1.5.5/...
  tar -zxvf filename
  ```
  * Download Apache Guacamole client source code
  ```sh
  cd /opt
  wget https://guacamole.apache.org/releases/1.5.5/...
  tar -zxvf filename
  ```
* Download LDAP Extension
  ```sh
  cd /opt
  wget https://guacamole.apache.org/releases/1.5.5/...
  tar -zxvf filename
  ```
* Download the SSO Extensions
```sh
cd /opt
wget https://guacamole.apache.org/releases/1.5.5/...
tar -zxvf filename
```
* Download and install Tomcat
  https://www.digitalocean.com/community/tutorials/how-to-install-apache-tomcat-9-on-debian-10
  
* Download and extract Java 16 (Java 17 led to errors)
```sh
cd /opt
wget https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-x64_bin.tar.gz
tar -zxvf filename
```
* Delete all extracted files
```sh
rm *.gz
```
### Server Prep
1. Statically assign NIC
2. Comment out all ipv6 entries in /etc/hosts (rdp won't work without this step)
3. Add JAVA_HOME path to your shell instance
   ```sh
   export JAVA_HOME=/opt/jdk-16.0.2
#### Installation of Dependencies

1. Download and install Cairo (Required dependency)
   ```sh
     sudo apt install libcairo2-dev -y
   ```
2. Download and install libjpeg-turbo (Required dependency)
   ```sh
     sudo apt install libjpeg62-turbo-dev -y
   ```
3. Download and install libpng (Required dependency)
   ```sh
     sudo apt install libpng-dev -y
   ```
4. Download and install libtool (Required dependency)
   ```sh
     sudo apt install libtool-bin -y
   ```
5. Download and install libuuid (Required dependency)
   ```sh
     sudo apt install uuid-dev -y
   ```
6. Download and install build-essential (Required dependency)
  ```sh
    sudo apt install build-essential -y
  ```
7. Download and install build-essential (Required dependency)
  ```sh
    sudo apt install maven -y
  ```

8. Download and install FFmpeg (Optional used for recording sessions)
   ```sh
     sudo apt install libavcodec-dev, libavformat-dev, libavutil-dev, libswscale-dev -y
   ```
9. Download and install FreeRDP (Optional but necessary dependency)
   ```sh
     sudo apt install freerdp2-dev -y
   ```
10. Download and install Pango (Optional but necessary dependency)
   ```sh
     sudo apt install libpango1.0-dev -y
   ```
11. Download and install libssh2 (Optional but necessary dependency)
   ```sh
     sudo apt install libssh2-1-dev -y
   ```
12. Download and install libVNCServer (Optional but necessary dependency)
   ```sh
     sudo apt install libvncserver-dev -y
   ```
13. Download and install PulseAudio (Optional but necessary dependency)
   ```sh
     sudo apt install libpulse-dev -y
   ```
14. Download and install OpenSSL (Optional but necessary dependency)
   ```sh
     sudo apt install libssl-dev -y
   ```
15. Download and install libvorbis (Optional but necessary dependency)
   ```sh
     sudo apt install libvorbis-dev -y
   ```
16. Download and install libwebp (Optional but necessary dependency)
   ```sh
     sudo apt install libwebp-dev -y
   ```
#### Building the Guacamole Server
1. Change into the Guacamole server directory
   ```sh
   cd /opt/guacamole-server-1.5.5/
   ```
2. Configure the application with with installed dependencies
   ```sh
   ./configure --with-init-dir=/etc/init.d
   ```
3. Compile and Install Guacamole
   ```sh
   make && make install
   ```
4. Enable the guacd Service at Startup
   ```sh
   systemctl enable guacd
   ```
#### Building the Guacmole Client
1. Change into the Guacamole client directory
```sh
cd /opt/guacamole-client-1.5.5/
```
2. Use Maven to Build the .war Guacamole Package
   ```sh
   mvn package
   ```
#### Deploy Guacamole
1. Copy .war Guacamole Client Package to Tomcat Webapp Directory
   ```sh
   cp /opt/guacamole-client-1.5.5/guacamole/target/guacamole-1.5.5.war /opt/tomcat/webapps/guacamole.war
   ```
2. Make Working Directory and Files (user-mapping.xml is only used for initial testing of RDP)
   ```sh
   mkdir /etc/guacamole
   mkdir /etc/guacamole/extensions
   mkdir /etc/guacamole/lib
   touch guacamole.properties
   touch logback.xml
   touch user-mapping.xml
   ```
3. Fill in the contents of the .xml files above with that of the files in this repository.
4. Restart Applicable Services
   ```sh
   systemctl restart guacd
   systemctl restart tomcat
   ```
5. Test RDP through Guacamole @ http://serverip:8080/guacamole

#### Setup LDAP Authentication
1. Copy the LDAP authentication extension to /etc/guacamole/extensions
   ```sh
   cp /opt/guacamole-auth-ldap-1.5.5/guacamole-1.5.5.war /etc/guacamole/extensions
   ``` 
2. Create a service account in the LDAP server. The service account only needs to have "Domain Users" permissions.
3. Update /etc/guacamolguacamole.properties with the ldap configurations in the file in this repository.
4. Restart the Tomcat service
   ```sh
   systemctl restart tomcat
   ```
#### Setup Database for Connection Configurations (So we are not using LDAP to store configurations)
1. Copy the JDBC authentication extension to /etc/guacamole/extensions
   ```sh
   cp /opt/guacamole-auth-jdbc-1.5.5/postgresql/guacamole-auth-jdbc-postgresql-1.5.5.jar /etc/guacamole/extensions/
   ```
2. Download the JDBC Driver and move it to /etc/guacamole/lib https://jdbc.postgresql.org/download/
3. Install the database program
   ```sh
   apt install postgres
   ```
4. Install sudo so we can use the initial postgres user
   ```sh
   apt install sudo
   ```
5. Become the initial postgres user
   ```sh
   su postgres
   ```
6. Create the Database
   ```sh
   createdb guacamole_db
   ```
7. Setup the DB Schema
   ```sh
   cd /opt/guacamole-auth-jdbc-1.5.5/postgresql
   cat schema/*.sql | psql -d guacamole_db -f -
   ```
8. Grant Guacamole Access to the DB
   ```sh
   psql -d guacamole_db
   CREATE USER guacamole_user WITH PASSWORD 'some_password';
   GRANT SELECT,INSERT,UPDATE,DELETE ON ALL TABLES IN SCHEMA public TO guacamole_user;
   GRANT SELECT,USAGE ON ALL SEQUENCES IN SCHEMA public TO guacamole_user;
   \q
   ```
9. Configure Guacamole to use the database in /etc/guacamole/guacamole.properites
10. Restart the Tomcat service
   ```sh
   systemctl restart tomcat
   ```
11. Create an admin user in LDAP, login as guacadmin and give the new admin user all admin permissions.
12. Login as the new admin and disable login for guacadmin.
#### Setup Reverse Proxy
1. Add the line, URIEncoding="UTF-8", to the connector configuration of Tomcat
   ```sh
   nano /opt/tomcat/conf/server.xml
   ```
   Find the following configuration and add the line above:
   ```sh
       <Connector port="8080" protocol="HTTP/1.1"
               connectionTimeout="20000"
               redirectPort="8443"
               maxParameterCount="1000"
               URIEncoding="UTF-8"
               />
   ```
2. Setup Remote IP Valve in Tomcat.
   ```sh
   nano /opt/tomcat/conf/server.xml
   ```
   Setup the following valve
   ```sh
   <Valve className="org.apache.catalina.valves.RemoteIpValve"
               internalProxies="127.0.0.1"
               remoteIpHeader="x-forwarded-for"
               remoteIpProxiesHeader="x-forwarded-by"
               protocolHeader="x-forwarded-proto" />
   ```
3. Setup the reverse proxy with the congiguration file in this repository
4. Get the Guacamole server a public certificate

#### Setup OIDC (Domain UPN Needs to match email domain when tieing in LDAP connections)
1. Copy the OIDC extenstion into /etc/gucamole/extensions
   ```sh
   cd /etc/opt/guacamole-auth-sso-1.5.5/openid
   cp guacamole-auth-sso-openid-1.5.5.jar /etc/guacamole/extensions/
   ```
2. Register the application in Azure (save your work at all necessary steps)
   - Login into https://entra.microsoft.com/
   - Navigate to Identity > Applications > App Registrations
   - Select "New Registration".
   - Redirect URI will be https://internal.domain.com/guacamole
   - Navigate to Certificates & Secrets and create a new client secret (copy the secret after creation).
   - Navigate to Authentication, select "ID Tokens" under Implicit grant and hybrid flows.
   - To get all necessary URLs for the next step, Navigate to Overview > Endpoints. Copy and paste the OpenID Connect metadata document URL into your browser. When you navigate to it, all needed information will be there - just ctrl + F.
4. Update the /etc/guacamole/guacamole.properties configuration with the values in the file in this repository.
5. Restart the Tomcat service
   ```sh
   systemctl restart tomcat
   ```
   
<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

_For more examples, please refer to the [Documentation](https://guacamole.apache.org/doc/1.5.5/gug/)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
<!-- ## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/dacapo59/guacamole/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p> -->



<!-- CONTRIBUTING -->
<!-- ## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p> -->



<!-- LICENSE -->
<!-- ## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p> -->



<!-- CONTACT -->
## Contact

<!-- Your Name - [@twitter_handle](https://twitter.com/twitter_handle) -brett@brettjoiner.me -->
Brett Joiner - [Email](https://twitter.com/twitter_handle) - brett@brettjoiner.me

Project Link: [https://github.com/dacapo59/guacamole](https://github.com/dacapo59/guacamole)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
<!-- ## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#readme-top">back to top</a>)</p> -->



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/dacapo59/Keycloak.svg?style=for-the-badge
[contributors-url]: https://github.com/dacapo59/Keycloak/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/dacapo59/Keycloak.svg?style=for-the-badge
[forks-url]: https://github.com/dacapo59/Keycloak/network/members
[stars-shield]: https://img.shields.io/github/stars/dacapo59/Keycloak.svg?style=for-the-badge
[stars-url]: https://github.com/dacapo59/Keycloak/stargazers
[issues-shield]: https://img.shields.io/github/issues/dacapo59/Keycloak.svg?style=for-the-badge
[issues-url]: https://github.com/dacapo59/Keycloak/issues
[license-shield]: https://img.shields.io/github/license/dacapo59/Keycloak.svg?style=for-the-badge
[license-url]: https://github.com/dacapo59/Keycloak/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/brett-joiner-100122b0
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com
[guacamole-url]: https://guacamole.apache.org/releases/1.5.5/
[guacamole-image]: https://guacamole.apache.org/images/logos/guac-tricolor-logo.svg
[tomcat-url]: https://tomcat.apache.org/tomcat-10.1-doc/index.html
[tomcat-image]: https://tomcat.apache.org/tomcat-10.1-doc/images/tomcat.png
