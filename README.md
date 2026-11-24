# Last Light — Wilderness Protocol

A dependency-free, single-player browser survival game prototype adapted from the supplied Roblox survival plan. Explore the valley, recover three supply caches, survive hostile scavengers and predators, and restore the radio relay. Mental stability affects aim and can be restored by breathing, food, and the safe camp.

## Play locally

Open `public/index.html` in a modern browser, or serve the project directory with any static file server. There is no build step or package installation.

### Controls

- **WASD / arrow keys:** move; **Shift:** sprint
- **Mouse:** aim and fire
- **E:** search a nearby cache, rest in the safe camp, or activate the relay
- **Hold B:** complete a 12-second controlled breathing cycle for 15 seconds of steadier aim
- **Q:** apply a pressure dressing; **T:** use a tourniquet on severe limb bleeding; **F:** eat a ration; **R:** reload

The prototype includes survival vitals, a safe zone and campfire, hostile encounters, supply caches, low-stability tremors and sensory effects, and recovery through breathing and supplies. Gunfire and predator attacks can cause location-specific wounds: ongoing blood loss, pain, and shock impair survival and control. Use **Q** to apply a pressure dressing or **T** to stop severe limb bleeding with a tourniquet. These are simplified game mechanics, not real-world medical instructions.

## Build and host on Cloudflare Workers

The game is a static site: there is no compile/build command. The repository includes `wrangler.jsonc`, which points Cloudflare Workers Static Assets at `public/`.

1. Install Node.js and sign in to a Cloudflare account.
2. From the repository root, run `npx wrangler@latest login` to authorize Wrangler.
3. Preview locally with `npx wrangler@latest dev`.
4. Publish with `npx wrangler@latest deploy`. Wrangler uploads the static game assets and prints the deployed `workers.dev` URL.

To publish changes, repeat the deploy command. A custom domain can be connected to the Worker from the Cloudflare dashboard.