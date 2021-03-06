# norns Athenaeum

A repository of study, spike, and sample scripts for [norns](https://monome.org/docs/norns/). Each was created as a means to learn different techniques or technologies myself. I am sharing it in the event others find them inspiring or useful.

## Scripts

- **arc.lua** - explores getting data from and updating the LEDs on an [arc](https://monome.org/docs/arc/). Handles linear "scaled rings", chunky "paginated rings", wrapping, "snap" LED aliasing, and encoder sensitivity. Additionally, arbitrary minimum and maximum values can be set for each encoder which will then scale out accordingly. Also, a utility function to map the current encoder value to a given segment.

- **crow.lua** - test script to make sure crow and Just Friends are working. One test is for volts/slew, another is for envelopes, another is for JF. Essentially just the code from [here](https://github.com/monome/crow-studies) but recoded as a "homework assignment."

- **delay.lua** - explores the concept of MIDI delay. Control rate and decay level of MIDI notes and get visual feedback as notes are toggled on and off. Requires an outboard MIDI device, preferably one capable of polyphony. Made as a research spike for a new [arcologies](https://github.com/tyleretters/arcologies) structure.

- **enc_wait.lua** - watches the norns encoders but lets you know _when_ they're turning and _when they've stopped_ turning. This allows for more sophisticated user interactions. This technology is what the arcologies UI is based on.

- **graphics.lua** - the Northern Information graphics library. These seven abstractractions are used in all Northern Information projects.

- **markov.lua** - simple markov chain implementation. supports any number of "links" and each link has a probability of repeating, advancing, and retreating.

- **ppqn.lua** - reliably sync multiple entities with a single clock using [PPQN](https://en.wikipedia.org/wiki/Pulses_per_quarter_note).

- **rotate.lua** - example of newly implemented `screen.rotate(degrees)` and `screen.translate(x, y)` functions.

- **splash.lua** - the Northern Information splash screen. The `graphics:splash()` method is where most of the action happens. Conceptually, the "NI" logo is always there but it is randomly revealed, concealed, and then inverted. Note: frames are used for sequencing but drawing needs to happen from "back to front." The logic mashes these two concepts together while favoring brevity over clarity. For example, right at the start we see `local l = globals.frame >= 49 and 0 or 15`, this is because after 49 frames the splash screen inverts black for white and white for black.

- **text_rotate.lua** - example of newly implemented `screen.text_rotate(x, y, str, degrees)` and `screen.text_center_rotate(x, y, str, degrees)` functions.

## Credits

Software design by [Tyler Etters](https://nor.the-rn.info).

<a href="https://nor.the-rn.info"><img src="https://northern-information.github.io/arcologies-docs/assets/images/northern-information.svg" alt="Northern Information" width="100"/></a>
