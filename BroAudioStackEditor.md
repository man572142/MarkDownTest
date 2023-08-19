<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
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

  <!-- PROJECT Title -->
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
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#quick-start">Quick Start</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
![Product Name Screen Shot][product-screenshot]

BroAudio is a sound management and playback tool for Unity. It is the only tool that cares about <a href="#sound-quality">sound quality</a> and prioritizes developer user experience. You can build a massive audio system without the need to learn complex middleware software (like FMOD or WWise). Build and mange library with zero code. Play and control the audio with only one line of code.


<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Features

- Seamless Loop
- Fade In/Out with multiple ease function
- Cross Fade
- Randomized (with weighted)
- Sequencer
- Visualized waveform and playback lines
- Playing across multiple scenes
- Clip Editor for permanent clip editing
- Low Code Design
- Customizable GUI settings
- and more…

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Quick Start -->
## Quick Start

### Creating sound libraries
Locate <i>BroAudio</i> in the Unity menu bar and open <b><i>LibraryManager</i></b> to create your sound libraries. This process does not require writing any code.

### Declare an AudioID and use BroAudio.Play() to play it 
![BasicAPI][basic-API-screenshot]

### Set the AudioID in the Inspector
![SetAudioID][set-audioid]

### Hit the Unity play button and enjoy it !
That's all you need to start using BroAudio. Of course, there are more than just this. Check out the documentation to fully unlock all the features of BroAudio.



## Installation

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


# Explanation

## Library Manager

### Asset
### Library

## Clip Editor

## Setting



<a name="sound-quality"></a>

## Why is this tool related to sound quality?

Indeed, apart from issues like noise and distortion that need to be repaired, there is no objective method to enhance sound quality. However, a playback system still holds significant impact over the quality of sound. This is because the loss of sound quality is relatively easy to occur and hard to avoid. That's why BroAudio consistently prioritizes preserving the original sound quality as its primary design consideration.


Here are some common issues listed along with how BroAudio addresses them:

| Issues | Bro's Solutions|
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
[basic-API-screenshot]: https://raw.githubusercontent.com/man572142/MarkDownTest/5860b913e1af0ea8bc3fbaad972b96df02eb3f8d/BasicAPI.svg
[set-audioid]: https://raw.githubusercontent.com/man572142/MarkDownTest/main/AudioID.gif