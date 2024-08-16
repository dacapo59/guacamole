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

* [![Keycloak][keycloak-image]][keycloak-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get started with installing Keycloak, first ensure you have administrative access to your server. Keycloak is an open-source identity and access management solution that provides comprehensive authentication and authorization capabilities. In a typical Keycloak setup, you deploy a Keycloak server that acts as a centralized identity provider, managing user identities, roles, and permissions. Keycloak supports various authentication protocols such as OAuth 2.0, OpenID Connect, and SAML, allowing seamless integration with diverse applications and services. Administrators can configure realms to manage different sets of users and applications, set up client applications with specific security settings, and establish federated identity providers to synchronize with existing identity systems. Additionally, Keycloak provides features like single sign-on (SSO), multi-factor authentication (MFA), and user federation, streamlining user management and enhancing security across your ecosystem.

### Prerequisites

* Debian OS
* Download Apache Guacamole server source code
  ```sh
  wget https://apache.org/dyn/closer.lua/guacamole/1.5.5/source/guacamole-server-1.5.5.tar.gz?action=download
  ```
### Installation

1. Download and install Cairo (Required dependency)
   ```sh
     sudo apt install libcairo2-dev
   ```
2. Download and install libjpeg-turbo (Required dependency)
   ```sh
     sudo apt install libjpeg62-turbo-dev
   ```
3. Download and install libpng (Required dependency)
   ```sh
     sudo apt install libpng-dev
   ```
4. Download and install libtool (Required dependency)
   ```sh
     sudo apt install libtool-bin
   ```
5. Download and install libuuid (Required dependency)
   ```sh
     sudo apt install uuid-dev
   ```
6. Download and install FFmpeg (Optional but necessary dependency)
   ```sh
     sudo apt install libavcodec-dev, libavformat-dev, libavutil-dev, libswscale-dev
   ```
7. Download and install FreeRDP (Optional but necessary dependency)
   ```sh
     sudo apt install freerdp2-dev
   ```
8. Download and install Pango (Optional but necessary dependency)
   ```sh
     sudo apt install libpango1.0-dev
   ```
9. Download and install libssh2 (Optional but necessary dependency)
   ```sh
     sudo apt install libssh2-1-dev
   ```
10. Download and install libVNCServer (Optional but necessary dependency)
   ```sh
     sudo apt install libvncserver-dev
   ```
11. Download and install PulseAudio (Optional but necessary dependency)
   ```sh
     sudo apt install libpulse-dev
   ```
12. Download and install OpenSSL (Optional but necessary dependency)
   ```sh
     sudo apt install libssl-dev
   ```
13. Download and install libvorbis (Optional but necessary dependency)
   ```sh
     sudo apt install libvorbis-dev
   ```
14. Download and install libwebp (Optional but necessary dependency)
   ```sh
     sudo apt install libwebp-dev
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

_For more examples, please refer to the [Documentation](https://www.keycloak.org/documentation)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
<!-- ## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/dacapo59/Keycloak/issues) for a full list of proposed features (and known issues).

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

Project Link: [https://github.com/dacapo59/Keycloak](https://github.com/dacapo59/Keycloak)

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
[keycloak-url]: https://www.keycloak.org/downloads
[keycloak-image]: https://www.keycloak.org/resources/images/icon.svg
[maxminddb-url]: https://www.maxmind.com/en/geoip-databases
[maxminddb-image]: https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQJ042SY-Km30dCaPnBcuIw-5u2mZjNqX6NHQ&s
