# Particle Motion UI for Background using React and tsParticles

Author:Pankaj Kumar Singh
:-
Project: Particle Motion UI
Live Link:https://react-tsparticles.netlify.app/


## Introduction

Welcome to the Particle Motion UI project! This project is dedicated to creating an engaging and visually appealing background using particle motion effects. We utilize the power of React, along with the tsParticles library, to bring life to your website's background.

With this project, you can add a touch of dynamism and interactivity to your web page, making it stand out and capture the attention of your visitors. The particles' fluid motion creates a sense of liveliness and adds a modern touch to your website's aesthetics.

## Features

- Fluid and dynamic particle motion in the background.
- Easy integration into any React-based website.
- Customizable particle behavior, colors, shapes, and sizes.
- Interactive and responsive design for various screen sizes.
- Lightweight and performant due to the optimized nature of tsParticles.


## Once the scripts are loaded you can set up tsParticles like this:

(async () => {
  await loadFull(tsParticles); // not needed if using the bundle script, required for any other installation

  await tsParticles.load({
    id: "tsparticles",
    options: {
      /* options */
    },
  });
})();

## Class Component

import React from "react";
import Particles from "react-particles";
import type { Engine } from "tsparticles-engine";
import { loadFull } from "tsparticles";

export class ParticlesContainer extends PureComponent<unknown> {
  // this customizes the component tsParticles installation
  async customInit(engine: Engine): Promise<void> {
    // this adds the bundle to tsParticles
    await loadFull(engine);
  }

  render() {
    const options = {
      /* custom options */
    };

    return <Particles options={options} init={this.customInit} />;
  }
}


## Customization

The `ParticleConfig.js` file contains various properties that you can tweak to customize the particle motion:

- `particlesNumber`: Number of particles on the screen.
- `particleSpeed`: Speed of particle movement.
- `particleColor`: Color of particles.
- ...and more.

Refer to the [tsParticles documentation](https://www.npmjs.com/package/tsparticles) for a comprehensive list of available customization options.

## Credits

This project was made possible by the collaboration of the React community and the tsParticles library.

- [React](https://reactjs.org/)
- [tsParticles](https://www.npmjs.com/package/tsparticles)

## Contribution

Contributions are welcome! If you find any issues or have ideas for improvements, please submit a pull request or open an issue in the repository.

## License

This project is under the [MIT License](LICENSE).

---

Thank you for choosing the One Step Ahead Particle Motion UI for your website! We hope it adds a delightful touch to your web presence. If you have any questions or need assistance, please feel free to reach out to us.

**Connect with Me**
- GitHub: [github.com/your-username](https://github.com/pankaj-2503)
- Email: pankajpj3103@gmail.com

