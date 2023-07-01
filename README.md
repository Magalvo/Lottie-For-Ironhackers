
# Lottie Files For Ironhackers

A brief explanation on how to use Lottie animations with React.





## Installation

Install the lottie-react dependency

```bash
  npm install lottie-react
```
    
## Documentation

1. Visit [LottieFiles](https://lottiefiles.com/) and find an animation that you like;

2. Click on the animation and download the Lottie JSON file;
![image](https://i.imgur.com/5ooX6Zi.png)


3. Crete a folder inside your SRC folder called e.g.: "lotties" and put the downloaded file directly in that folder.

4. To display the animation On your desired page/component you will need to do the following:

- First import the necessary dependency:

```bash
  import Lottie from 'lottie-react';
```
- Import the desired .json file of the animation that you want to display:

```bash
  import animationData from '../lotties/dog.json';
```

- Inside your React Function Component add the following constant:

```bash
  const defaultOptions = {
    loop: true,
    autoplay: true,
    rendererSettings: {
      preserveAspectRatio: 'xMidYMid slice'
    }
  };
```
(This will set some rendering options for your animation that you can latter change as you desire);

- Add the Lottie component on your code and add the necessary props, preferebly inside a div so it doesn’t mess with the stylings . Make the necessary adjsutements to the styling:


```bash
  <div className='animation' style={{ height: '600px', width: '600px' }}>
          <Lottie
            options={defaultOptions}
            animationData={animationData}
            height={600}
            width={600}
          />
        </div>
```

Here you can see the full code of the page:

```bash
import React from 'react';
import '../App.css';
import Lottie from 'lottie-react';
import animationData from '../lotties/dog.json';
import 'bootstrap/dist/css/bootstrap.min.css';

const Banner = () => {
  const defaultOptions = {
    loop: true,
    autoplay: true,
    rendererSettings: {
      preserveAspectRatio: 'xMidYMid slice'
    }
  };

  return (
    <>
      <div
        id='home'
        className='container d-flex justify-content-center align-items-center'
        style={{ height: '100vh' }}
      >
        <div className='animation' style={{ height: '600px', width: '600px' }}>
          <Lottie
            options={defaultOptions}
            animationData={animationData}
            height={600}
            width={600}
          />
        </div>
        <h1 style={{ color: '#6985ce' }}>
          We Are Working Tirelessly <br />
          <span style={{ color: '#77AA68' }}>
            <b>To Launch This Pawsome Site</b>
          </span>
        </h1>
      </div>
      <hr style={{ width: '500px', color: '#6985ce', heigth: '50px' }} />
    </>
  );
};

export default Banner;

```
A final look of the animation 😁

![image](https://i.imgur.com/VBNFARq.gif)

You can also use this as a loading screen the process would be pretty much the same.

Happy Hacking!









## Appendix

[Lottie Documentation](https://lottiefiles.com/)


## Feedback

If you have any questions, please reach out to me I'll be happy to help 🚀

## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://magalvo.com/)

[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/diogomagalhaescalvo/)


