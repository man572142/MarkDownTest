﻿<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
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
  <a href="https://github.com/man572142/Bro_Audio">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTkLLebM2iyUEOjlEfGYApDzHgeyMvBneukFw&usqp=CAU" alt="Logo" width="128" height="128">
  </a>

<h3 align="center">BroAudio</h3>

  <p align="center">A simple and intutive Audio Middleware for Unity
    <br />
    <a href="https://github.com/man572142/Bro_Audio"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/man572142/Bro_Audio">View Demo</a>
    ·
    <a href="https://github.com/man572142/Bro_Audio/issues">Report Bug</a>
    ·
    <a href="https://github.com/man572142/Bro_Audio/issues">Request Feature</a>
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
[![Product Name Screen Shot][product-screenshot]](https://example.com)

BroAudio is a sound management and playback tool for Unity. It is the only tool that cares about <a href="#SoundQuality">sound quality</a>and prioritizes developer user experience. You can build a massive audio system without the need to learn complex middleware software (like FMOD or WWise). Build and mange library with zero code. Play and control the audio with only one line of code.



<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/man572142/Bro_Audio.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```js
   const API_KEY = 'ENTER YOUR API';
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Why is this tool related to sound quality?
<a name="SoundQuality"></a>
In fact, once a sound is recorded or produced, unless there are issues that need to be repaired (like noise, distortion, etc.), the quality of a normal audio cannot be objectively improved. However, reducing the quality of a sound is relatively easy and hard to avoid. This is why preserving the original quality as much as possible is a primary design consideration for BroAudio. This is not an easy task, as every stage of playback can have varying degrees of impact on the quality.

| Issues | Solutions|
| -- | -- | 
| Distortion caused by playing multiple sounds simultaneously. | Well-designed mixer and auto-ducking on the master track |
|Comb Filtering / Haas Effect|Preventing rapid repetition of the same sound|
|Unbalanced volume levels|Highly adaptable real-time volume control system|
|Unnatural volume changes in Fade In, Fade Out and CrossFade|Utilizing AudioMixer for volume control|

 
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ROADMAP -->
## Roadmap

- [ ] Feature 1
- [ ] Feature 2
- [ ] Feature 3
    - [ ] Nested Feature

See the [open issues](https://github.com/man572142/Bro_Audio/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Che Hsiang Weng - man572142@gmail.com

Project Link: [https://github.com/man572142/Bro_Audio](https://github.com/man572142/Bro_Audio)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* []()
* []()
* []()

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/man572142/Bro_Audio.svg?style=for-the-badge
[contributors-url]: https://github.com/man572142/Bro_Audio/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/man572142/Bro_Audio.svg?style=for-the-badge
[forks-url]: https://github.com/man572142/Bro_Audio/network/members
[stars-shield]: https://img.shields.io/github/stars/man572142/Bro_Audio.svg?style=for-the-badge
[stars-url]: https://github.com/man572142/Bro_Audio/stargazers
[issues-shield]: https://img.shields.io/github/issues/man572142/Bro_Audio.svg?style=for-the-badge
[issues-url]: https://github.com/man572142/Bro_Audio/issues
[license-shield]: https://img.shields.io/github/license/man572142/Bro_Audio.svg?style=for-the-badge
[license-url]: https://github.com/man572142/Bro_Audio/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/linkedin_username
[product-screenshot]: https://raw.githubusercontent.com/man572142/MarkDownTest/main/LibraryManager_Shadow.png
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