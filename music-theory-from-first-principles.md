# MUSIC THEORY FROM FIRST PRINCIPLES

*Building harmony, melody, and rhythm from integers and algorithms*

A complete reconstruction of Western music theory using pitch classes 0-11,
modular arithmetic, and algorithmic thinking

---

# Table of Contents

- [Introduction](#introduction)
- [Part I: SOUND AND NUMBER](#part-i-sound-and-number)
  - [I.A. What You Hear When You Hear a Note](#ia-what-you-hear-when-you-hear-a-note)
  - [I.B. The Octave: Where Numbers Circle Back](#ib-the-octave-where-numbers-circle-back)
  - [I.C. Twelve Pitch Classes](#ic-twelve-pitch-classes)
  - [I.D. The Two-Component System](#id-the-two-component-system)
  - [I.E. From Two Components to Frequency](#ie-from-two-components-to-frequency)
  - [I.F. The MIDI Number](#if-the-midi-number)
  - [I.G. Notation Reference](#ig-notation-reference)
- [Part II: INTERVALS AND DISTANCE](#part-ii-intervals-and-distance)
  - [II.A. Semitones and the Distance Function](#iia-semitones-and-the-distance-function)
  - [II.B. Interval Names as Aliases](#iib-interval-names-as-aliases)
  - [II.C. Complementary Intervals](#iic-complementary-intervals)
  - [II.D. Consonance, Dissonance, and Simple Ratios](#iid-consonance-dissonance-and-simple-ratios)
  - [II.E. Compound Intervals](#iie-compound-intervals)
  - [II.F. Interval Vectors](#iif-interval-vectors)
- [Part III: SCALES](#part-iii-scales)
  - [III.A. Scales as Subsets of Z₁₂](#iiia-scales-as-subsets-of-z12)
  - [III.B. The Major Scale Algorithm](#iiib-the-major-scale-algorithm)
  - [III.C. The Three Minor Scales](#iiic-the-three-minor-scales)
  - [III.D. Pentatonic and Blues Scales](#iiid-pentatonic-and-blues-scales)
  - [III.E. Chromatic and Whole-Tone Scales](#iiie-chromatic-and-whole-tone-scales)
  - [III.F. Scale Comparison by Interval Content](#iiif-scale-comparison-by-interval-content)
- [Part IV: KEYS AND KEY SIGNATURES](#part-iv-keys-and-key-signatures)
  - [IV.A. Keys as Rooted Scales](#iva-keys-as-rooted-scales)
  - [IV.B. Sharps, Flats, and the Spelling Convention](#ivb-sharps-flats-and-the-spelling-convention)
  - [IV.C. Enharmonic Equivalence](#ivc-enharmonic-equivalence)
  - [IV.D. Relative and Parallel Keys](#ivd-relative-and-parallel-keys)
- [Part V: THE CIRCLE OF FIFTHS](#part-v-the-circle-of-fifths)
  - [V.A. Generating Z₁₂ by Repeated Addition of 7](#va-generating-z12-by-repeated-addition-of-7)
  - [V.B. The Circle as a Graph](#vb-the-circle-as-a-graph)
  - [V.C. Key Signatures on the Circle](#vc-key-signatures-on-the-circle)
  - [V.D. Tritone Symmetry](#vd-tritone-symmetry)
  - [V.E. Applications of the Circle](#ve-applications-of-the-circle)
- [Part VI: MODES](#part-vi-modes)
  - [VI.A. Modes as Rotations](#via-modes-as-rotations)
  - [VI.B. The Seven Diatonic Modes](#vib-the-seven-diatonic-modes)
  - [VI.C. Modal Brightness Ordering](#vic-modal-brightness-ordering)
  - [VI.D. Modes Beyond the Diatonic](#vid-modes-beyond-the-diatonic)
- [Part VII: CHORDS](#part-vii-chords)
  - [VII.A. Chords as Pitch-Class Sets](#viia-chords-as-pitch-class-sets)
  - [VII.B. Triads: The Four Types](#viib-triads-the-four-types)
  - [VII.C. Seventh Chords](#viic-seventh-chords)
  - [VII.D. Inversions and Voicings](#viid-inversions-and-voicings)
  - [VII.E. Extended Chords: Ninths, Elevenths, Thirteenths](#viie-extended-chords-ninths-elevenths-thirteenths)
  - [VII.F. Suspended and Added-Tone Chords](#viif-suspended-and-added-tone-chords)
  - [VII.G. Building Chords on Scale Degrees](#viig-building-chords-on-scale-degrees)
- [Part VIII: HARMONIC FUNCTION AND PROGRESSIONS](#part-viii-harmonic-function-and-progressions)
  - [VIII.A. Tonic, Subdominant, Dominant](#viiia-tonic-subdominant-dominant)
  - [VIII.B. Diatonic Chord Progressions](#viiib-diatonic-chord-progressions)
  - [VIII.C. The V-I Resolution](#viiic-the-v-i-resolution)
  - [VIII.D. Circle Progressions](#viiid-circle-progressions)
  - [VIII.E. Secondary Dominants](#viiie-secondary-dominants)
  - [VIII.F. Common Progressions as Algorithms](#viiif-common-progressions-as-algorithms)
  - [VIII.G. Non-Functional Harmony](#viiig-non-functional-harmony)
- [Part IX: TRANSPOSITION AND MODULATION](#part-ix-transposition-and-modulation)
  - [IX.A. Transposition as Addition in Z₁₂](#ixa-transposition-as-addition-in-z12)
  - [IX.B. Transposing Melodies and Chords](#ixb-transposing-melodies-and-chords)
  - [IX.C. Common Modulation Techniques](#ixc-common-modulation-techniques)
  - [IX.D. Pivot Chords](#ixd-pivot-chords)
  - [IX.E. Modulation Distance](#ixe-modulation-distance)
- [Part X: RHYTHM, METER, AND DURATION](#part-x-rhythm-meter-and-duration)
  - [X.A. Beat, Pulse, and Tempo](#xa-beat-pulse-and-tempo)
  - [X.B. Meter and Time Signatures](#xb-meter-and-time-signatures)
  - [X.C. Note Durations as Fractions](#xc-note-durations-as-fractions)
  - [X.D. Tuplets and Subdivision](#xd-tuplets-and-subdivision)
  - [X.E. Syncopation and Displacement](#xe-syncopation-and-displacement)
  - [X.F. Polyrhythm and Polymeter](#xf-polyrhythm-and-polymeter)
- [Part XI: FORM AND STRUCTURE](#part-xi-form-and-structure)
  - [XI.A. Phrases, Periods, and Sentences](#xia-phrases-periods-and-sentences)
  - [XI.B. Binary Form (AB)](#xib-binary-form-ab)
  - [XI.C. Ternary Form (ABA)](#xic-ternary-form-aba)
  - [XI.D. Rondo (ABACA...)](#xid-rondo-abaca)
  - [XI.E. Sonata-Allegro Form](#xie-sonata-allegro-form)
  - [XI.F. Theme and Variations](#xif-theme-and-variations)
  - [XI.G. The 12-Bar Blues](#xig-the-12-bar-blues)
- [Part XII: TEXTURE, COUNTERPOINT, AND SET THEORY](#part-xii-texture-counterpoint-and-set-theory)
  - [XII.A. Dynamics and Articulation](#xiia-dynamics-and-articulation)
  - [XII.B. Timbre and Tone Color](#xiib-timbre-and-tone-color)
  - [XII.C. Texture](#xiic-texture)
  - [XII.D. Counterpoint Basics](#xiid-counterpoint-basics)
  - [XII.E. Pitch Class Set Theory](#xiie-pitch-class-set-theory)
- [Glossary](#glossary)
- [Bibliography](#bibliography)

---

## Introduction

Pick up any music theory textbook and the first thing it teaches is the musical alphabet: A, B, C, D, E, F, G. Seven letters, cycling forever. It seems simple. But within minutes, complications arrive. The distance from C to D is two semitones. The distance from E to F is one. The distance from F to G is two again. Nothing in the letters signals which gaps are wide and which are narrow. The naming system treats unequal intervals as though they were equal steps, and the student is left to memorize which pairs of letters happen to sit closer together.

It gets worse. Between most letter-named notes sit sharps and flats: between C and D there is C♯ (equivalently, D♭). But between B and C, and between E and F, there is no such in-between note. The alphabet implies seven evenly spaced pitches. The piano keyboard reveals twelve unevenly named ones. A beginner confronting this mismatch has two choices: accept the naming conventions as historical inheritance and memorize the exceptions, or look for a system where the structure is visible from the start.

This book takes the second path.

The situation is a bit like Roman numerals. Roman numerals work. People did mathematics with them for centuries. But try long division in Roman numerals and the notation fights the computation at every step. Arabic numerals did not change what numbers are. They changed how easily the structure of numbers could be seen and manipulated. The move from letter names to integers is the same kind of shift: not a new theory but a better notation, one that makes existing structure visible instead of hiding it behind historical convention.

The core idea is simple. Instead of seven letters with accidentals patched on, number the twelve notes of the chromatic scale 0 through 11. In this system, every pair of adjacent numbers is separated by the same interval: one semitone. The distance from any note to any other note is found by subtraction. Scales become sets of integers. Chords become sets of integers. Transposition becomes addition. The entire apparatus of Western music theory, from key signatures to counterpoint, can be rebuilt on this foundation with no ambiguity about spacing, no special cases for B-C and E-F, and no need to memorize which notes are "natural" and which require accidentals.

The letter names will not disappear from this book. They are the lingua franca of musicians everywhere, printed on sheet music, displayed on guitar tuners, called out in rehearsals. To ignore them would be impractical. But they will appear as correspondences, translations, annotations in the margin. The primary language will be integers, because integers make structure visible.

A concrete illustration of what gets hidden. In the letter system, the C major scale is C, D, E, F, G, A, B. The D major scale is D, E, F♯, G, A, B, C♯. These look like different objects with different rules: why does D major need sharps when C major does not? In the integer system, the C major scale is {0, 2, 4, 5, 7, 9, 11}. The D major scale is {2, 4, 6, 7, 9, 11, 1}. Both are generated by the same interval pattern (2, 2, 1, 2, 2, 2, 1) applied starting from different roots. The sharps were never special rules. They were artifacts of the naming system. The integer representation reveals that all major scales are the same shape, placed at different starting positions on the circle.

Consider a preview. The note that most of the world calls "middle C" becomes the pair (4, 0): octave 4, pitch class 0. The note called "A above middle C," the standard tuning reference at 440 Hz, becomes (4, 9): same octave, pitch class 9. The distance between them is 9 semitones. No need to count letter names and remember which gaps are wide. Subtraction gives the answer directly.

This two-component notation, an octave number paired with a pitch class, captures everything a note name does and more. It separates the two perceptual dimensions of pitch: which register a note lives in (the octave) and which position it occupies within that register (the pitch class). From these two components, every other quantity follows by arithmetic. Frequency in hertz, MIDI note number, interval size, scale membership: all are computed, not looked up.

The mathematical setting for pitch classes is Z₁₂, the integers modulo 12. This is the same structure as a clock face: after 11 comes 0 again. Adding 7 to pitch class 8 gives pitch class 3, because 15 mod 12 = 3. The circle of fifths, one of music theory's most celebrated diagrams, turns out to be the sequence generated by repeatedly adding 7 in Z₁₂. Modes are rotations of a set. Transposition is translation. Inversion is negation. The algebraic language is not a metaphor laid over music. It is the structure that conventional notation partially obscures.

None of this requires advanced mathematics. Modular arithmetic is clock arithmetic. Set membership is list-checking. The algorithms in this book use nothing beyond addition, subtraction, multiplication, division, and the modulo operation. A reader comfortable with basic algebra will find every derivation followable. A reader with programming experience will recognize the algorithms as directly implementable. The goal is not abstraction for its own sake but clarity: to present music theory in a form where every rule has a reason and every pattern has a computation behind it.

Here is the plan.

**Part I: Sound and Number** starts with physical vibration and builds up to the twelve pitch classes, the two-component notation system, and the formula connecting pitch to frequency. By the end of Part I, every note on a piano has a precise numerical address and a computable frequency.

**Part II: Intervals and Distance** defines the distance between notes as subtraction, maps these distances to traditional interval names, and introduces the concepts of consonance and dissonance through frequency ratios.

**Part III: Scales** treats scales as subsets of Z₁₂ and derives the major scale, three forms of the minor scale, pentatonic, blues, chromatic, and whole-tone scales from interval patterns.

**Part IV: Keys and Key Signatures** connects scales to the system of sharps and flats, explains enharmonic equivalence, and establishes the relationship between relative and parallel keys.

**Part V: The Circle of Fifths** reveals the circle as a consequence of repeatedly adding 7 mod 12 and demonstrates its applications for understanding key relationships.

**Part VI: Modes** presents the seven diatonic modes as rotations of a single interval pattern and extends the idea to non-diatonic modes.

**Part VII: Chords** builds triads, seventh chords, and extended chords from pitch-class sets, with inversions and voicings treated as rearrangements of set elements.

**Part VIII: Harmonic Function and Progressions** assigns functional roles to chords and models common progressions as algorithms, including secondary dominants and non-functional harmony.

**Part IX: Transposition and Modulation** formalizes transposition as addition in Z₁₂ and catalogs modulation techniques with their algorithmic descriptions.

**Part X: Rhythm, Meter, and Duration** extends the mathematical treatment to the time dimension, modeling durations as fractions and exploring syncopation, polyrhythm, and polymeter.

**Part XI: Form and Structure** treats musical form as higher-level algorithms operating on phrases, sections, and movements.

**Part XII: Texture, Counterpoint, and Set Theory** covers polyphonic writing, species counterpoint, pitch-class set theory, twelve-tone technique, and the symmetry groups that unify them.

A glossary and bibliography close the book.

One final note before the first section. This book is a reconstruction, not a revolution. Every concept here has a traditional counterpart. The major scale is still the major scale. A dominant seventh chord still resolves to the tonic. What changes is the lens. Where traditional theory says "go up a fifth," this book says "add 7 mod 12." Where traditional theory says "the relative minor is three half-steps below the major," this book says "subtract 3 from the root pitch class." The musical knowledge is the same. The notation makes the patterns computable.

Readers with programming backgrounds will find these algorithms directly implementable. Readers who are practicing musicians will find familiar terrain described in unfamiliar but precise language. Readers coming to music theory for the first time will, with any luck, be spared some of the memorization that traditional presentations require, because in this system the patterns explain themselves.

---

# Part I: SOUND AND NUMBER

## I.A. What You Hear When You Hear a Note

A guitar string is plucked. It vibrates. The vibration pushes and pulls at the surrounding air, creating a pressure wave that radiates outward, reaches an ear, and registers as sound. The speed of the vibration determines what a listener perceives as the pitch of the note: fast vibration sounds high, slow vibration sounds low.

The physical quantity behind pitch is frequency, measured in hertz (Hz): the number of complete vibration cycles per second.[^1] A string vibrating 261.63 times per second produces the note that musicians call middle C. A string vibrating 440 times per second produces the A above middle C, the note used worldwide as a tuning reference.[^2] A string vibrating 82.41 times per second produces the lowest note on a standard guitar.

These are precise numbers, and precision matters, because the relationships between frequencies are what give music its structure. The interval between two notes is not determined by the difference between their frequencies but by the ratio. Middle C at 261.63 Hz and the A above it at 440 Hz have a frequency ratio of 440 / 261.63 ≈ 1.6818. That ratio, not the difference of 178.37 Hz, is what the ear perceives as the musical distance between them.

This is worth pausing on. If two notes have frequencies 200 Hz and 300 Hz, the ratio is 3:2 and the interval sounds like a perfect fifth. If two other notes have frequencies 400 Hz and 600 Hz, the ratio is still 3:2, and the interval sounds the same, even though the difference has doubled from 100 Hz to 200 Hz. Pitch perception is logarithmic: the ear measures ratios, not gaps.[^3]

A single vibrating string also does something subtle. It vibrates not just at one frequency but at many simultaneously: the fundamental frequency and a series of overtones at integer multiples of that fundamental. A string with fundamental frequency 100 Hz also vibrates at 200 Hz, 300 Hz, 400 Hz, and so on, each overtone progressively quieter. This harmonic series is not an abstraction. It is the physical reason why certain frequency ratios sound consonant. The ratio 2:1 (the octave) is the relationship between the first overtone and the fundamental. The ratio 3:2 (the fifth) is the relationship between the second overtone and the first. The most consonant intervals in music correspond to the simplest ratios in the harmonic series.[^4]

The distinction between a note's fundamental and its overtones also explains why a piano and a violin playing the same pitch sound different. Both produce the same fundamental frequency, but the relative strengths of their overtones differ. The piano's hammered string emphasizes certain overtones; the bowed string of a violin emphasizes others. This is timbre: the color or quality of a sound, determined by the overtone profile. Timbre is the reason musical instruments are distinguishable. It is also the reason that two instruments playing the same note still sound like two distinct voices.

For now, the essential facts are three. Sound is vibration. Frequency measures the speed of vibration. Pitch perception tracks the ratios between frequencies.

## I.B. The Octave: Where Numbers Circle Back

Play a note at 261.63 Hz. Now play the note at 523.25 Hz. The ratio is 523.25 / 261.63 ≈ 2.0000. These two notes, one exactly twice the frequency of the other, sound so similar that musicians give them the same name. The lower one is called C. The higher one is also called C, just "an octave higher."

This is not a convention arbitrarily imposed. It reflects something deep about auditory perception. When a man and a woman sing the same melody "in unison," they are typically singing an octave apart, the woman's voice roughly double the frequency of the man's. They hear themselves as singing the same notes. Children singing along with adults do the same thing without instruction. The octave is the most fundamental equivalence in pitch perception: two frequencies related by a factor of 2 are heard as the same note in different registers.[^5]

This equivalence has a profound structural consequence. Pitch is not a line stretching from low to high. It is a helix. Moving upward in frequency, a listener passes through the same twelve pitch positions over and over, each time one octave higher. The pitch class (which of the twelve positions) stays the same while the octave (which loop of the helix) advances. A note at 130.81 Hz, a note at 261.63 Hz, and a note at 523.25 Hz are all "the same note" in the sense that matters for harmony and melody. They differ only in register.

Formally: two frequencies f₁ and f₂ are octave-equivalent if f₂ / f₁ = 2^k for some integer k. This is an equivalence relation (reflexive, symmetric, transitive), and it partitions the infinite range of audible frequencies into equivalence classes.[^6] Each equivalence class is a pitch class. The entire machinery of scales, chords, and keys operates on pitch classes, not on specific frequencies. When a theory book says "the C major scale contains C, D, E, F, G, A, B," it is naming seven pitch classes, each of which appears in every octave.

The helix image is worth holding onto. Imagine a spiral staircase viewed from the side: it goes up and up, but viewed from above, it traces the same circle repeatedly. Pitch works the same way. The "going up" is octave register. The "circle" is the twelve pitch classes. Most of music theory lives on the circle.

The word "octave" itself comes from the Latin for "eighth," because in the seven-note scales that dominate Western music, the eighth note in the scale is a return to the first note one octave higher. The name is a remnant of the letter system, where counting from C to the next C passes through eight letter names (C, D, E, F, G, A, B, C). In the integer system, there is no reason to call it "eighth." The octave is simply the interval of 12 semitones, the distance from any pitch class back to itself in the next register. But the traditional name is too deeply embedded to displace, and using it causes no confusion as long as the underlying arithmetic is clear.

## I.C. Twelve Pitch Classes

Why twelve? The question has a long history and multiple answers, none entirely complete.[^7] The pragmatic answer is that twelve equally spaced divisions of the octave produce a collection of intervals that closely approximate the simple frequency ratios (3:2, 4:3, 5:4) found in the harmonic series, while keeping the number of distinct notes manageable. Fewer divisions and the approximations suffer. More divisions and the system becomes unwieldy for instruments with fixed pitch (pianos, guitars, flutes). Twelve is a sweet spot, and Western music has settled on it so thoroughly that it forms the background assumption of virtually all theory, composition, and instrument design since the eighteenth century.[^8]

In equal temperament, the octave is divided into twelve equal parts. "Equal" here means equal in the logarithmic sense that governs pitch perception: each step multiplies the frequency by the same factor. Since twelve such steps must multiply to 2 (one octave), each step multiplies by 2^(1/12), the twelfth root of 2, approximately 1.05946.[^9]

The twelve pitch classes are numbered 0 through 11. The correspondence to traditional letter names is:

| Pitch class | Letter name(s) |
|:-----------:|:--------------|
| 0           | C              |
| 1           | C♯ / D♭       |
| 2           | D              |
| 3           | D♯ / E♭       |
| 4           | E              |
| 5           | F              |
| 6           | F♯ / G♭       |
| 7           | G              |
| 8           | G♯ / A♭       |
| 9           | A              |
| 10          | A♯ / B♭       |
| 11          | B              |

Several things are visible in this table that the letter-name system obscures. The distance from E (4) to F (5) is 1, the same as the distance from C (0) to C♯ (1). In the letter system, these feel like different kinds of step: E to F is a "natural" half step, while C to C♯ involves an accidental. In the integer system, both are simply +1. The distance from C (0) to D (2) is 2, the same as from D (2) to E (4). Same gap, same number. No exceptions, no special cases.

The choice of 0 for C is conventional, aligning with the fact that C major is the scale with no sharps or flats in traditional notation. Any pitch class could serve as 0, but using C keeps the correspondence with standard practice transparent.[^10]

Note that pitch classes 1, 3, 6, 8, and 10 each carry two letter names (a sharp and a flat). These pairs are enharmonic equivalents: different names for the same pitch. In the integer system, enharmonic equivalence is trivial. There is no C♯ versus D♭ debate. There is only pitch class 1.

The frequency ratio between any two adjacent pitch classes is 2^(1/12) ≈ 1.05946. This means that moving up one pitch class multiplies the frequency by about 5.946%. Moving up two pitch classes multiplies by (2^(1/12))² = 2^(2/12) = 2^(1/6) ≈ 1.12246, or about 12.2%. Moving up seven pitch classes (what traditional theory calls a perfect fifth) multiplies by 2^(7/12) ≈ 1.49831, very close to the "pure" ratio of 3:2 = 1.5 from the harmonic series. The twelve-tone equal temperament system sacrifices the purity of these simple ratios by a tiny amount in exchange for the ability to play in any key and transpose freely. The compromise, formalized in the eighteenth century, made the modern piano possible and opened the door to the rich modulatory language of classical and popular music alike.

## I.D. The Two-Component System

A pitch class identifies a position on the circle. To identify a specific note, a specific key on a piano, a specific frequency, the octave is also needed. The two-component representation of a note is the ordered pair (o, p), where o is the octave number and p is the pitch class (0 through 11).

Middle C, by convention, is (4, 0): octave 4, pitch class 0. From this anchor point, every other note on the piano receives a unique address. The C one octave below middle C is (3, 0). The A used for tuning, 440 Hz, is (4, 9). The lowest note on a standard 88-key piano is (0, 9), corresponding to the A at 27.5 Hz. The highest note is (8, 0), the C at 4186.01 Hz.

**Worked Example 1.** What is the two-component representation of the F♯ above middle C? F♯ has pitch class 6. It is in the same octave as middle C (octave 4) because the octave number increments at C (pitch class 0). So the representation is (4, 6).

**Worked Example 2.** What about the B just below middle C? B has pitch class 11. Since it is below middle C, it falls in the octave below: (3, 11).

The octave boundary rule is worth stating explicitly: octave o contains the notes from (o, 0) through (o, 11). The note (o, 0) is the C that begins octave o, and (o, 11) is the B that ends it. This means every C starts a new octave.[^11]

A few more landmarks, for reference:

| Note (common name)     | Two-component | Comment                          |
|:----------------------|:------------:|:---------------------------------|
| Lowest piano note      | (0, 9)       | A at 27.5 Hz                     |
| Lowest C on piano      | (1, 0)       | Two octaves below middle C (approximately) |
| Open low E on guitar   | (2, 4)       | Standard tuning                  |
| Open A on guitar       | (2, 9)       | Standard tuning                  |
| Open D on guitar       | (3, 2)       | Standard tuning                  |
| Open G on guitar       | (3, 7)       | Standard tuning                  |
| Open B on guitar       | (3, 11)      | Standard tuning                  |
| Open high E on guitar  | (4, 4)       | Standard tuning                  |
| Middle C               | (4, 0)       | 261.63 Hz                        |
| A440                   | (4, 9)       | Tuning standard                  |
| Soprano high C         | (5, 0)       | "High C" in vocal music          |
| Highest piano note     | (8, 0)       | C at 4186.01 Hz                  |

The two-component system carries exactly as much information as a traditional note name with an octave subscript (C₄, A₄, and so on), but it makes computation straightforward. Distances, transpositions, and frequency conversions all reduce to arithmetic on the two components.

**Worked Example 3.** The six open strings of a guitar in standard tuning are (2, 4), (2, 9), (3, 2), (3, 7), (3, 11), (4, 4). Reading off the pitch classes: 4, 9, 2, 7, 11, 4. Looking up the correspondence table: E, A, D, G, B, E. The intervals between adjacent strings (computed by subtracting consecutive note numbers) are: 5, 5, 5, 4, 5. Five semitones, five, five, four, five. That single "4" between the G and B strings is why guitarists have to adjust fingering patterns when crossing that boundary. The two-component system makes the asymmetry visible as a number.

## I.E. From Two Components to Frequency

Given a note (o, p), its frequency in hertz is:

f = f₀ × 2^(o + p/12)

The constant f₀ is the frequency of (0, 0), the C in octave 0. To find it, start from the known reference: A440 is (4, 9), so:

440 = f₀ × 2^(4 + 9/12)

Solving for f₀:

f₀ = 440 / 2^(4 + 9/12) = 440 / 2^(4.75)

Computing 2^(4.75): this is 2^4 × 2^(0.75) = 16 × 2^(3/4). Now, 2^(3/4) = (2^(1/4))³. The fourth root of 2 is approximately 1.18921, so 2^(3/4) ≈ 1.68179. Therefore 2^(4.75) ≈ 16 × 1.68179 ≈ 26.9087.

f₀ = 440 / 26.9087 ≈ 16.3516 Hz

This frequency is far below the threshold of human hearing (roughly 20 Hz), which makes sense: (0, 0) is a C well below any note on a piano. The lowest note on a standard piano, A0 = (0, 9), has a frequency of 27.5 Hz, barely audible and felt as much as heard. The constant f₀ exists as a mathematical anchor, not a musical one.[^12]

The formula f = f₀ × 2^(o + p/12) encodes the entire equal-temperament pitch system in a single expression. It says: start at f₀, double the frequency o times (to reach the right octave), then multiply by 2^(p/12) (to reach the right pitch class within that octave). The exponent o + p/12 is the total number of octaves above f₀, expressed as a decimal. For (4, 0), that is 4.0 octaves. For (4, 6), it is 4.5 octaves, exactly halfway between octave 4 and octave 5 in the logarithmic sense. Pitch class 6 (F♯/G♭) sits at the midpoint of the octave. This is the tritone, and its position at the exact halfway point will become important in later sections.

> **Algorithm: Two-Component to Frequency**
>
> **Input:** A note represented as (o, p), where o is the octave number and p is the pitch class (0-11). A reference frequency f₀ ≈ 16.3516 Hz.
>
> **Output:** The frequency f in hertz.
>
> **Step 1.** Compute the exponent: e = o + p/12.
>
> **Step 2.** Compute the frequency: f = f₀ × 2^e.

**Worked Example 4.** Convert middle C, (4, 0), to a frequency.

e = 4 + 0/12 = 4.0

f = 16.3516 × 2^4 = 16.3516 × 16 = 261.626 Hz

This matches the known frequency of middle C. ✓

**Worked Example 5.** Convert (4, 9) to a frequency, as a consistency check.

e = 4 + 9/12 = 4.75

f = 16.3516 × 2^(4.75) = 16.3516 × 26.9087 ≈ 440.00 Hz

Exactly the tuning standard. ✓

**Worked Example 6.** Find the frequency of the open low E string on a guitar, (2, 4).

e = 2 + 4/12 = 2 + 0.3333 = 2.3333

2^(2.3333) = 2^2 × 2^(1/3) = 4 × 1.2599 ≈ 5.0397

f = 16.3516 × 5.0397 ≈ 82.41 Hz

This is the standard frequency for E2. ✓

The reverse direction, from frequency to two-component, inverts the formula:

o + p/12 = log₂(f / f₀)

Given the result r = log₂(f / f₀), the octave is o = ⌊r⌋ (the integer part), and the pitch class is p = round(12 × (r − o)), where rounding to the nearest integer handles any tiny floating-point discrepancies.

**Worked Example 7.** A note has frequency 329.63 Hz. What is its two-component representation?

r = log₂(329.63 / 16.3516) = log₂(20.1587)

log₂(20.1587) = ln(20.1587) / ln(2) ≈ 3.0037 / 0.6931 ≈ 4.3333

o = ⌊4.3333⌋ = 4

p = round(12 × 0.3333) = round(4.0) = 4

The note is (4, 4), pitch class 4, which corresponds to E. And 329.63 Hz is indeed E4. ✓

## I.F. The MIDI Number

The two-component representation keeps octave and pitch class distinct, which is useful for most theoretical purposes. But sometimes a single integer is more convenient, for instance when computing the distance between two notes or when communicating with digital music systems. The two-component form separates the circular part (pitch class) from the linear part (octave). A single integer collapses them back together, unrolling the helix into a straight line.

The note number n linearizes the two-component representation:

n = 12o + p

This maps each note to a unique non-negative integer. The inverse is:

o = ⌊n / 12⌋

p = n mod 12

In this system, middle C = (4, 0) has note number 48. The A at 440 Hz = (4, 9) has note number 57. The lowest piano note (0, 9) has note number 9.

**Worked Example 8.** Compute the note number for the open D string on a guitar, (3, 2).

n = 12 × 3 + 2 = 38

**Worked Example 9.** A note has note number 64. What is its two-component representation and letter name?

o = ⌊64 / 12⌋ = 5

p = 64 mod 12 = 4

The note is (5, 4), pitch class 4, which corresponds to E. This is E5, the E one octave above the E just above middle C.

One complication deserves mention. The MIDI standard, the protocol that electronic instruments and computers use to communicate note information, also assigns integers to notes, but with a different octave convention. In MIDI, middle C is note number 60, not 48.[^13] The discrepancy arises because the MIDI standard numbers octaves starting from -1 rather than 0, effectively adding 1 to the octave number throughout. In MIDI's scheme, middle C is in "octave 5" and its note number is 12 × 5 + 0 = 60.

This book uses the convention that middle C = (4, 0) = note number 48, which keeps octave numbering aligned with the most common practice in music theory (where middle C is called C4). When interfacing with MIDI hardware or software, add 12 to the note numbers used here. The conversion is trivial:

n_MIDI = n + 12

n = n_MIDI − 12

The note number makes distance computation immediate. The interval between two notes, measured in semitones, is the absolute difference of their note numbers.

**Worked Example 10.** How many semitones separate middle C from A440?

Middle C: n = 48. A440: n = 57. Distance = |57 − 48| = 9 semitones.

**Worked Example 11.** How many semitones span the entire 88-key piano, from (0, 9) to (8, 0)?

Lowest note: n = 12 × 0 + 9 = 9. Highest note: n = 12 × 8 + 0 = 96. Span = 96 − 9 = 87 semitones.

Eighty-eight keys, eighty-seven intervals between them. The arithmetic checks out.

The note number also makes it easy to express frequency directly, without passing through the two-component form. Substituting o = ⌊n / 12⌋ and p = n mod 12 into the frequency formula yields:

f = f₀ × 2^(n/12)

This is the same formula, just with the two components recombined. It says that frequency doubles for every increase of 12 in the note number, which is exactly what it means to move up one octave.

> **Algorithm: Note Number to Frequency**
>
> **Input:** A note number n. A reference frequency f₀ ≈ 16.3516 Hz.
>
> **Output:** The frequency f in hertz.
>
> **Step 1.** Compute f = f₀ × 2^(n/12).

When the direction of the interval matters (up versus down), use the signed difference n₂ − n₁ rather than the absolute value. A positive result means an ascending interval; negative means descending. When only the pitch-class relationship matters (ignoring octave), reduce the interval mod 12: the interval class between pitch classes p₁ and p₂ is (p₂ − p₁) mod 12, always a value from 0 to 11.

**Worked Example 12.** What is the interval class from pitch class 9 (A) to pitch class 2 (D)?

(2 − 9) mod 12 = (−7) mod 12 = 5

The interval class is 5 semitones (a perfect fourth in traditional terminology). The mod operation ensures the result is always non-negative, measuring the ascending distance around the circle from the first pitch class to the second.

## I.G. Notation Reference

The following table consolidates the notation introduced in Part I. For each pitch class, it shows the letter name, the note in octave 4 in two-component form, its note number, its frequency, and its identity as an element of Z₁₂.

Z₁₂ = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11} is the set of integers modulo 12. Addition in Z₁₂ wraps around: 9 + 5 = 14 ≡ 2 (mod 12). Subtraction wraps the other way: 3 − 7 = −4 ≡ 8 (mod 12). This is the algebraic structure that governs pitch-class arithmetic throughout the rest of the book.[^14] It behaves like a clock with 12 positions. Position 0 sits where 12 o'clock would be, and counting proceeds clockwise.

| p (Z₁₂ element) | Letter name(s) | (4, p) | Note number | Frequency (Hz) |
|:---:|:---|:---:|:---:|---:|
| 0  | C          | (4, 0)  | 48 | 261.63 |
| 1  | C♯ / D♭   | (4, 1)  | 49 | 277.18 |
| 2  | D          | (4, 2)  | 50 | 293.66 |
| 3  | D♯ / E♭   | (4, 3)  | 51 | 311.13 |
| 4  | E          | (4, 4)  | 52 | 329.63 |
| 5  | F          | (4, 5)  | 53 | 349.23 |
| 6  | F♯ / G♭   | (4, 6)  | 54 | 369.99 |
| 7  | G          | (4, 7)  | 55 | 392.00 |
| 8  | G♯ / A♭   | (4, 8)  | 56 | 415.30 |
| 9  | A          | (4, 9)  | 57 | 440.00 |
| 10 | A♯ / B♭   | (4, 10) | 58 | 466.16 |
| 11 | B          | (4, 11) | 59 | 493.88 |

Each frequency is computed from f = 16.3516 × 2^(4 + p/12). The values match standard equal-temperament tuning tables to the precision shown.[^15]

The table repays careful examination. Notice that the frequency roughly doubles from pitch class 0 (261.63 Hz) to the C that would begin the next octave (523.25 Hz, not shown). Notice that the note numbers in octave 4 run from 48 to 59, a span of 12, exactly one octave's worth. Notice that the frequency ratios between adjacent rows are all equal to 2^(1/12) ≈ 1.05946, confirming equal temperament. And notice how much information is packed into the pair (4, p): from it, the note number, frequency, and pitch-class identity all follow by simple arithmetic.

**Worked Example 13.** Verify that the frequency ratio between G (p = 7) and C (p = 0) in the table above approximates 3:2.

392.00 / 261.63 ≈ 1.4983

The pure ratio 3:2 = 1.5000. The equal-temperament approximation is off by about 0.11%, inaudible in practice.

The key formulas from Part I, collected:

**Frequency from two-component:**
f = f₀ × 2^(o + p/12), where f₀ ≈ 16.3516 Hz

**Note number from two-component:**
n = 12o + p

**Two-component from note number:**
o = ⌊n / 12⌋, p = n mod 12

**Interval (in semitones) between two notes:**
|n₂ − n₁|

**Interval class between two pitch classes:**
(p₂ − p₁) mod 12

**Octave equivalence:**
Two frequencies are octave-equivalent iff their ratio is 2^k for integer k.

**Equal temperament step ratio:**
2^(1/12) ≈ 1.05946

With these tools in hand, every note has an address, every address has a frequency, and every pair of notes has a computable distance. The groundwork is laid. Part II will put that distance to work, defining intervals and exploring what makes some of them consonant and others tense.

# Part II: INTERVALS AND DISTANCE

## II.A. Semitones and the Distance Function

Part I gave every note a numerical address. Now those addresses earn their keep. The most basic question two notes raise is: how far apart are they?

The atomic unit of distance in the twelve-tone system is the semitone, the gap between any two adjacent pitch classes. From 0 to 1, from 7 to 8, from 11 back around to 0: each of these is one semitone, one step on the circle of Z₁₂. Every larger interval is a count of semitones. There is no smaller subdivision in standard Western music.[^16]

But "distance" is not a single concept. It splits into two distinct measurements depending on whether octave and direction matter.

The first measurement uses note numbers. Given two notes with note numbers n₁ and n₂, the signed interval is n₂ − n₁. A positive result means n₂ is higher than n₁ (ascending). A negative result means n₂ is lower (descending). The magnitude |n₂ − n₁| gives the absolute distance in semitones, regardless of direction. This measurement is unbounded: the interval between the lowest and highest notes on a piano is 87 semitones, as computed in Worked Example 11. Note-number intervals carry full information about register, direction, and size.

The second measurement discards octave information and works entirely within Z₁₂. Given two pitch classes p and q, the directed pitch-class interval upward is (q − p) mod 12. This counts how many semitones you traverse going up (clockwise on the circle) from p to q. The directed interval downward is (p − q) mod 12, counting semitones going the other direction. These two quantities always sum to 12, unless both are 0 (which happens only when p = q). If the upward interval from p to q is 4, the downward interval is 8. Four steps clockwise, eight steps counterclockwise: they meet at the same destination.

Often, the direction does not matter. A composer who places two notes 4 semitones apart cares about the sound of that interval, not whether it was measured up or down. For this purpose, the interval class is defined as the smaller of the two directed intervals: min((q − p) mod 12, (p − q) mod 12). The interval class is always a value from 0 to 6. Values above 6 are impossible because if one direction measures more than 6, the other direction must measure less than 6 (since they sum to 12).

The three levels of measurement form a hierarchy. Note-number intervals are the most specific: they encode direction, magnitude, and register. Directed pitch-class intervals discard octave but preserve direction, answering the question "how far up (or down) on the circle?" Interval classes discard both octave and direction, retaining only the "size" of the gap: "how close together are these two pitch classes, by the shortest path?"

Each level is useful in different contexts. When analyzing a melody's contour (whether it rises, falls, leaps, or steps), note-number intervals matter. When identifying a chord type (major triad, minor seventh, and so on), interval classes suffice. When describing the relationship between two keys, directed pitch-class intervals capture the musical sense of "going up a fifth" versus "going down a fourth," even though both connect the same pitch classes.

**Worked Example 14.** Find all three interval measurements from pitch class 0 to pitch class 9. The directed interval upward is (9 − 0) mod 12 = 9. The directed interval downward is (0 − 9) mod 12 = 3. Check: 9 + 3 = 12. The interval class is min(9, 3) = 3. In traditional terms, 9 semitones up is a major sixth; 3 semitones down is a minor third. They connect the same two pitch classes.

**Worked Example 15.** Find all three interval measurements from pitch class 4 to pitch class 11. Upward: (11 − 4) mod 12 = 7. Downward: (4 − 11) mod 12 = (−7) mod 12 = 5. Check: 7 + 5 = 12. Interval class: min(7, 5) = 5. The interval class between pitch classes 4 and 11 is 5, regardless of which direction you measure.

## II.B. Interval Names as Aliases

Every interval in the twelve-tone system is fully specified by a semitone count. The number 7 tells you exactly how the two notes relate in frequency (a ratio of 2^(7/12) ≈ 1.498), how they sit on the pitch-class circle (seven steps apart), and how they will sound (consonant, stable, open). No additional information is needed.

Traditional music theory, however, has given each interval a name, and those names are so entrenched in musical communication that ignoring them would be impractical. The mapping is:

| Semitones | Interval name        | Abbreviation |
|:---------:|:---------------------|:------------:|
| 0         | Perfect unison       | P1           |
| 1         | Minor second         | m2           |
| 2         | Major second         | M2           |
| 3         | Minor third          | m3           |
| 4         | Major third          | M3           |
| 5         | Perfect fourth       | P4           |
| 6         | Tritone              | A4 / d5      |
| 7         | Perfect fifth        | P5           |
| 8         | Minor sixth          | m6           |
| 9         | Major sixth          | M6           |
| 10        | Minor seventh        | m7           |
| 11        | Major seventh        | M7           |
| 12        | Perfect octave       | P8           |

The names group into two families. The "perfect" intervals (0, 5, 7, and 12 semitones) are so called because they were historically considered the most stable and pure consonances. They do not come in major/minor pairs. The remaining intervals come in pairs: minor second and major second (1 and 2), minor third and major third (3 and 4), minor sixth and major sixth (8 and 9), minor seventh and major seventh (10 and 11). In each pair, "major" is the wider version by exactly one semitone.

The tritone at 6 semitones sits alone, belonging to neither family. Its name means "three whole tones" (three steps of 2 semitones each: 2 + 2 + 2 = 6). It divides the octave exactly in half. Historically, it was considered so dissonant that medieval theorists called it the *diabolus in musica*, the devil in music. The abbreviation reflects its ambiguous identity: it can be spelled as an augmented fourth (A4, four letter-name steps inflated by a semitone) or a diminished fifth (d5, five letter-name steps contracted by a semitone). In the integer system, this spelling distinction vanishes. There is only the number 6.

For readers who find it useful to anchor these intervals to sound, well-known melodies can serve as reference points. The minor second (1 semitone) is the menacing two-note alternation from the *Jaws* theme: two adjacent pitch classes, grinding against each other. The major second (2 semitones) opens "Happy Birthday" (the first two notes, "Hap-py," are a whole step apart). The minor third (3 semitones) is the descending call of "Hey Jude" at the word "Jude," or the "ding-dong" interval of a doorbell. The major third (4 semitones) opens "When the Saints Go Marching In" (the interval from "Oh" to "when"). The perfect fourth (5 semitones) opens "Here Comes the Bride" and also "Amazing Grace." The tritone (6 semitones) opens "The Simpsons" theme ("The Simp-") and also appears at the start of "Maria" from *West Side Story*. The perfect fifth (7 semitones) opens the *Star Wars* main theme and "Twinkle, Twinkle, Little Star" (from "Twin-" to "-kle"). The minor sixth (8 semitones) opens the love theme from *The Entertainer*. The major sixth (9 semitones) opens "My Bonnie Lies Over the Ocean." The minor seventh (10 semitones) opens the original *Star Trek* theme (the first two sung notes of "Space, the final frontier" in the vocal version). The major seventh (11 semitones) is the rarest as a melodic opener but appears between the first two notes of "Take On Me" by a-ha in certain transcriptions. The octave (12 semitones) opens "Somewhere Over the Rainbow."

These are mnemonics, not definitions. The definition is always the semitone count. But having a sonic reference for each interval makes recognition faster, and trained musicians internalize these associations until hearing a major sixth instantly retrieves the number 9 and vice versa.

Notice that the naming system carries redundancy. Saying "a perfect fifth" conveys exactly the same information as saying "7 semitones." The names add no content that the numbers lack. What they add is communicative convenience. Musicians think and talk in interval names, and reading a score requires recognizing them. This book will use both, preferring the integer when computing and the name when the context is musical.

One subtlety: the table above maps each semitone count to a single interval name, but traditional theory allows multiple names for the same semitone count depending on how the notes are spelled. The interval from C to G♯ (8 semitones) is called an augmented fifth, while the interval from C to A♭ (also 8 semitones) is called a minor sixth. Since both land on pitch class 8, and since this book treats enharmonic spellings as aliases for the same pitch class, these distinctions collapse. Eight semitones is eight semitones. The integer system is mercifully unambiguous.

## II.C. Complementary Intervals

Take any interval d (measured in semitones, 0 through 12). Its complement is d' = 12 − d. Together, d and d' sum to one octave. One measures the distance going up from the lower note to the higher; the other measures the distance continuing up from the higher note to the lower note's octave equivalent.

The complement pairs are:

| Interval | Complement | Sum |
|:---------|:-----------|:---:|
| P1 (0)   | P8 (12)    | 12  |
| m2 (1)   | M7 (11)    | 12  |
| M2 (2)   | m7 (10)    | 12  |
| m3 (3)   | M6 (9)     | 12  |
| M3 (4)   | m6 (8)     | 12  |
| P4 (5)   | P5 (7)     | 12  |
| tritone (6) | tritone (6) | 12 |

Several patterns emerge. Major intervals pair with minor intervals, and the quality flips: a major second's complement is a minor seventh, not a major seventh. Perfect intervals pair with other perfect intervals. The tritone, sitting at 6, is its own complement: 6 + 6 = 12. It is the only interval with this property, a consequence of its position at the exact midpoint of the octave.

The complement relationship has musical weight beyond the arithmetic. An interval and its complement share a family resemblance. A minor third (3 semitones) and a major sixth (9 semitones) connect the same two pitch classes, just in opposite directions. They tend to appear in similar harmonic contexts and evoke related moods. This is why inverting a chord (moving one of its notes up or down an octave) changes the voicing but preserves the chord's identity: the new intervals are complements of the old ones, connecting the same pitch classes.

In Z₁₂, complementation is additive inversion. The complement of d is −d (mod 12), because d + (−d) ≡ 0 (mod 12), and adding 0 in Z₁₂ is the same as completing the circle. This is not a coincidence. It is the reason the complement relationship is so structurally clean. Every property of complements follows from the group structure of Z₁₂: there are twelve elements, each has a unique additive inverse, and the inverse of the inverse is the original. The symmetry of the complement table is the symmetry of the group.

## II.D. Consonance, Dissonance, and Simple Ratios

Some intervals sound restful. Others sound tense. The terms for these qualities, consonance and dissonance, are among the oldest in music theory, and the question of why certain intervals sound consonant has occupied theorists since Pythagoras.

The physical explanation begins with frequency ratios. In Part I, the formula f = f₀ × 2^(n/12) established that equal temperament divides the octave into twelve logarithmically equal steps. But equal temperament is an approximation of something older: the pure intervals derived from the harmonic series, where frequency ratios are simple fractions.

The pure ratios for the most common intervals are:

| Interval | Pure ratio | Decimal | ET approximation (2^(d/12)) | ET decimal |
|:---------|:----------:|:-------:|:---------------------------:|:----------:|
| P8       | 2:1        | 2.0000  | 2^(12/12) = 2              | 2.0000     |
| P5       | 3:2        | 1.5000  | 2^(7/12)                   | 1.4983     |
| P4       | 4:3        | 1.3333  | 2^(5/12)                   | 1.3348     |
| M3       | 5:4        | 1.2500  | 2^(4/12)                   | 1.2599     |
| m3       | 6:5        | 1.2000  | 2^(3/12)                   | 1.1892     |
| M6       | 5:3        | 1.6667  | 2^(9/12)                   | 1.6818     |
| m6       | 8:5        | 1.6000  | 2^(8/12)                   | 1.5874     |

The pattern is striking. The most consonant intervals correspond to the simplest ratios. The octave (2:1) is the most consonant interval, so perfectly fused that two notes an octave apart are heard as "the same note." The perfect fifth (3:2) is the next most consonant: stable, open, the foundation of power chords in rock and of the harmonic language of virtually every musical tradition worldwide. The perfect fourth (4:3) is nearly as consonant. The major third (5:4) and minor third (6:5) are consonant but warmer, more colorful, carrying a quality of sweetness or melancholy that the bare fifth lacks.

The simpler the ratio, the more the overtone series of the two notes align. Two notes a perfect fifth apart share many overtones: the third harmonic of the lower note matches the second harmonic of the upper note. This overlap produces a sensation of blend, the two sounds locking together as though they belong to a single complex tone. Two notes a major third apart also share overtones, though fewer and higher in the series (the fifth harmonic of the lower note matches the fourth of the upper). The blend is still present but less pronounced, and the ear hears the interval as sweet rather than bare.

Two notes a minor second apart share almost no overtones in their lower partials, and the slight frequency difference between their fundamentals produces a pulsating interference called beating. If the two frequencies are 261 Hz and 277 Hz, the difference is 16 Hz, and the ear perceives a rapid pulsation at that rate. This beating is the physical correlate of roughness, and roughness is what the ear reports as dissonance.[^17] As the two frequencies move further apart, the beating accelerates beyond the range where the ear tracks individual pulses, and the roughness subsides. This is why a minor second (1 semitone) sounds rougher than a major second (2 semitones), even though both are classified as dissonant.

A rough consonance ranking, from most to least consonant:

1. P1 / P8 (unison, octave)
2. P5 (perfect fifth)
3. P4 (perfect fourth)
4. M3, m3 (major and minor thirds)
5. M6, m6 (major and minor sixths)
6. M2, m7 (major second, minor seventh)
7. m2, M7 (minor second, major seventh)
8. Tritone

This ranking is approximate. Context matters enormously: a minor second played slowly between two sustained strings sounds grating, but the same interval in a fast melodic passage sounds perfectly natural. Cultural familiarity also shapes perception. Jazz musicians hear major sevenths as lush and desirable; a listener trained only on medieval music might hear them as harsh. The ranking above reflects a broad consensus, not a physical law.

**Worked Example 16.** Verify the equal-temperament approximation for the perfect fifth and the major third.

For the perfect fifth (7 semitones): 2^(7/12). Compute 7/12 = 0.58333. Then 2^(0.58333) ≈ 1.4983. The pure ratio is 1.5000. The difference is 0.0017, or about 0.11%. For practical purposes, indistinguishable.

For the major third (4 semitones): 2^(4/12) = 2^(1/3) ≈ 1.2599. The pure ratio is 5/4 = 1.2500. The difference is 0.0099, or about 0.79%. Larger than the fifth's error, and in fact audible to trained ears in sustained chords. This is why barbershop quartets and string ensembles sometimes adjust their major thirds downward slightly, toward the pure ratio, when no keyboard instrument forces equal temperament on them.

**Worked Example 17.** Verify the perfect fourth. 2^(5/12). Compute 5/12 = 0.41667. Then 2^(0.41667) ≈ 1.3348. The pure ratio is 4/3 ≈ 1.3333. The difference is 0.0015, about 0.11%, matching the fifth's error. This is expected: the fourth and fifth are complements (5 + 7 = 12), so their equal-temperament errors are related by the same complementary structure.

The tension between pure ratios and equal temperament is one of the deep compromises in Western music. Pure intervals sound better in isolation but make free transposition impossible: a keyboard tuned to pure intervals in the key of C will sound noticeably out of tune in the key of F♯. Equal temperament distributes the impurity evenly across all keys, so that no key sounds perfectly pure and no key sounds terrible. The twelve-tone system, as described in this book, assumes equal temperament throughout. The pure ratios appear as the motivation for why certain intervals are consonant, but the mathematics of pitch classes operates in the equal-temperament world where 7 semitones is exactly 2^(7/12), not exactly 3/2.

## II.E. Compound Intervals

Every interval discussed so far fits within a single octave: 0 through 12 semitones. But notes can be more than 12 semitones apart, and the intervals beyond the octave have their own names and uses.

A compound interval is any interval larger than an octave. It is named by adding an octave (or multiples of an octave) to a simple interval. The most commonly encountered compound intervals are:

| Semitones | Name          | = Simple interval + octave |
|:---------:|:--------------|:---------------------------|
| 13        | Minor ninth   | m2 + P8 (1 + 12)          |
| 14        | Major ninth   | M2 + P8 (2 + 12)          |
| 15        | Minor tenth   | m3 + P8 (3 + 12)          |
| 16        | Major tenth   | M3 + P8 (4 + 12)          |
| 17        | Perfect eleventh | P4 + P8 (5 + 12)       |
| 21        | Minor thirteenth | m6 + P8 (8 + 12)       |
| 22        | Major thirteenth | M6 + P8 (9 + 12)       |

The pitch-class interval is invariant under octave displacement. A minor second (1 semitone) and a minor ninth (13 semitones) connect the same two pitch classes. Reducing mod 12, both yield 1. This is the formal content of octave equivalence: compound intervals reduce to their simple counterparts in the pitch-class world.

In practice, though, compound intervals do not sound identical to their simple counterparts. A minor second, with two adjacent pitch classes crammed into the same octave, sounds harsh and tense. A minor ninth, with the same two pitch classes separated by more than an octave, sounds spacious and atmospheric, almost lush. Jazz pianists exploit this distinction constantly: a left-hand root with a right-hand note a ninth above produces warmth, while the same two pitch classes played as a second would produce a crunch. The pitch-class content is the same, but the registral spread changes the perceptual character. This is one of the places where the distinction between note-number intervals and pitch-class intervals matters. Pitch-class theory says they are "the same interval." A composer's ear says they are related but distinct.

Compound intervals become especially important in the context of extended chords, which stack thirds beyond the seventh. A ninth chord adds a note 14 semitones above the root (a major ninth, or equivalently, a major second placed in the octave above). An eleventh chord adds 17 semitones. A thirteenth chord adds 21 or 22. These structures will be built systematically in Part VII. For now, the essential point is the relationship: every compound interval has a simple-interval kernel found by reducing mod 12, and the compound version adds registral space to the same pitch-class relationship.

**Worked Example 18.** A note number of 48 (middle C) and a note number of 62. What is the interval?

62 − 48 = 14 semitones. This is a major ninth. Reducing mod 12: 14 mod 12 = 2 semitones, which is a major second. The two notes are pitch classes 0 and 2 (C and D), separated by more than an octave.

## II.F. Interval Vectors

When analyzing not just a pair of notes but a collection of them, a useful tool is the interval vector, which tallies how many of each interval class appear among all pairs in the set.

Given a set of pitch classes S with |S| = k, there are k(k − 1)/2 unordered pairs. For each pair, compute the interval class (a value from 1 to 6). The interval vector is the six-element list [n₁, n₂, n₃, n₄, n₅, n₆], where nᵢ is the number of pairs with interval class i.

The interval vector ignores interval class 0 (pairs of identical pitch classes), since a set does not contain duplicates. It also folds the twelve directed intervals into six interval classes, using the convention that interval classes above 6 are reduced to their complement. Seven semitones (P5) becomes interval class 5. Eight semitones becomes interval class 4. And so on.

**Worked Example 19.** Compute the interval vector of the major triad {0, 4, 7}.

There are 3 pitch classes, so 3(2)/2 = 3 pairs:

- 0 and 4: (4 − 0) mod 12 = 4, (0 − 4) mod 12 = 8, interval class = min(4, 8) = 4
- 0 and 7: (7 − 0) mod 12 = 7, (0 − 7) mod 12 = 5, interval class = min(7, 5) = 5
- 4 and 7: (7 − 4) mod 12 = 3, (4 − 7) mod 12 = 9, interval class = min(3, 9) = 3

One pair at IC 3, one at IC 4, one at IC 5. The vector is [0, 0, 1, 1, 1, 0].

**Worked Example 20.** Compute the interval vector of the minor triad {0, 3, 7}.

Three pairs:

- 0 and 3: interval class = min(3, 9) = 3
- 0 and 7: interval class = min(7, 5) = 5
- 3 and 7: (7 − 3) mod 12 = 4, (3 − 7) mod 12 = 8, interval class = min(4, 8) = 4

The vector is [0, 0, 1, 1, 1, 0].

This is the same vector as the major triad. Major and minor triads contain exactly the same interval classes, in the same quantities, just arranged differently. A major triad has the major third (IC 4) on the bottom and the minor third (IC 3) on top; a minor triad reverses the arrangement. But the total interval content is identical. This is not a coincidence. The minor triad is the inversion of the major triad: {0, 3, 7} is obtained from {0, 4, 7} by applying the operation p → (12 − p) mod 12 and then transposing. Inversion preserves interval-class content, always. This deep symmetry will be explored fully in Part XII, when pitch-class set theory is developed.

The interval vector serves as a fingerprint for a pitch-class set. Two sets with the same vector share the same "palette" of intervallic relationships, even if they sound different in context. Two sets with different vectors have genuinely different intervallic characters. In Part III, the interval vector will be applied to scales, revealing why different scale types produce such different musical flavors.

---

# Part III: SCALES

## III.A. Scales as Subsets of Z₁₂

A scale is an ordered subset of Z₁₂. This definition is short, but it carries a great deal of structure.

The ordering is given by a step pattern: a sequence of positive integers that describes the intervals between consecutive scale degrees, proceeding upward from the root. The step pattern must sum to 12, ensuring that the scale spans exactly one octave and cycles back to its starting pitch class. The constraint that steps are positive means no pitch class is repeated and no step is skipped: the scale moves strictly upward (mod 12) from one degree to the next.

A scale with root r and step pattern [s₁, s₂, ..., sₖ] generates the pitch-class set:

{r, (r + s₁) mod 12, (r + s₁ + s₂) mod 12, ..., (r + s₁ + s₂ + ... + sₖ₋₁) mod 12}

The number k of steps equals the number of notes in the scale. The root r is the first degree, and applying the steps cumulatively produces the remaining degrees. Ascending through the scale means applying the steps in the given order. Descending means reversing the step order (most scales are symmetric in this regard, though the melodic minor will provide a notable exception).

This formulation separates structure from position. The step pattern determines the scale type: it defines the arrangement of wide and narrow intervals that gives the scale its characteristic sound. The root determines which pitch classes participate. A major scale rooted on 0 and a major scale rooted on 7 share the same step pattern and therefore the same internal structure. They differ only in which twelve pitch classes are selected.

This abstraction also makes comparison straightforward. Two scales can be compared by their step patterns, by their pitch-class content, by their interval vectors. Relationships between scale types (relative major and minor, modes, supersets and subsets) become operations on step patterns or pitch-class sets.

One clarification on ordering. A scale is "ordered" in the sense that it has a root and a direction (ascending from that root). The pitch-class set {0, 2, 4, 5, 7, 9, 11} can represent C major or, with a different root, A natural minor. The set alone does not determine the scale. The root and the step pattern together do. This is why scale construction is defined as a process (apply steps from root) rather than simply as a set membership condition. Two scales can share every pitch class and still sound profoundly different, because the root establishes which note is "home," and the step pattern, read from that home note, determines the sequence of tensions and resolutions the ear follows.

The next five sections apply this framework to the scales that form the backbone of Western music.

## III.B. The Major Scale Algorithm

The major scale is defined by the step pattern [2, 2, 1, 2, 2, 2, 1]. Seven steps, seven notes, summing to 12. The two single-semitone steps (each 1) sit between degrees 3-4 and degrees 7-1, creating the characteristic two-tetrachord structure: a group of four notes, a whole-step bridge, and another group of four notes with the same internal pattern.

> **Algorithm: Build Major Scale**
>
> **Input:** A root pitch class r (0-11).
>
> **Output:** An ordered set of 7 pitch classes forming the major scale on r.
>
> **Step 1.** Initialize the scale: S = [r].
>
> **Step 2.** Define the step pattern: steps = [2, 2, 1, 2, 2, 2, 1].
>
> **Step 3.** For i = 1 to 6: compute the next pitch class as (S[i−1] + steps[i−1]) mod 12. Append it to S.
>
> **Step 4.** Return S.

**Worked Example 21.** Build the major scale on root 0 (C).

Starting at 0, applying steps [2, 2, 1, 2, 2, 2, 1]:

- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 1 = 5
- 5 + 2 = 7
- 7 + 2 = 9
- 9 + 2 = 11

Scale: {0, 2, 4, 5, 7, 9, 11}. In letter names: C, D, E, F, G, A, B. The scale with no sharps or flats, the one that every piano beginner learns first.

**Worked Example 22.** Build the major scale on root 7 (G).

Starting at 7:

- 7 + 2 = 9
- 9 + 2 = 11
- 11 + 1 = 0
- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 2 = 6

Scale: {7, 9, 11, 0, 2, 4, 6}. In letter names: G, A, B, C, D, E, F♯. The mod 12 wraparound at 11 + 1 = 12 ≡ 0 is seamless. The single departure from the C major pitch classes, pitch class 6 (F♯) in place of pitch class 5 (F), is the one sharp in the key of G major.

Both scales share the step pattern [2, 2, 1, 2, 2, 2, 1]. The intervals between consecutive degrees are identical. This is what it means to say they are "the same scale" rooted on different pitch classes. The pattern is the invariant; the root is the variable.

The major scale has a deep connection to the circle of fifths, which Part V will develop fully. A preview is worth including here because it reveals that the step pattern [2, 2, 1, 2, 2, 2, 1] is not arbitrary. It is the inevitable consequence of a simple generation rule.

Take pitch class 5 (F). Add 7 repeatedly, reducing mod 12: 5, 0, 7, 2, 9, 4, 11. That is seven pitch classes, each a perfect fifth above the previous one. Now sort them into ascending order within a single octave: {0, 2, 4, 5, 7, 9, 11}. This is the C major scale. The step pattern between consecutive members is 2, 2, 1, 2, 2, 2, 1, exactly the major scale formula.

Try again starting from pitch class 0 (C). Add 7 six times: 0, 7, 2, 9, 4, 11, 6. Sorted: {0, 2, 4, 6, 7, 9, 11}. The step pattern: 2, 2, 2, 1, 2, 2, 1. This is the G major scale (root 7), not C major. The root of the resulting major scale depends on where the sequence of seven fifths begins. Specifically, the root is always the second element in the sequence (the first fifth above the starting point).

The pattern holds universally. Any seven consecutive pitch classes on the circle of fifths, when sorted, produce a major scale. The two half-steps in the pattern always appear at the positions where the chain of fifths begins and ends, because those are the only places where the sorted sequence has adjacent pitch classes separated by 5 fifths-worth of gap (which, after sorting, compresses to a single semitone). The elegance of this derivation is that it reduces the entire major scale to a single operation: "collect seven adjacent fifths." Everything else follows.

## III.C. The Three Minor Scales

The minor scale comes in three variants, each modifying the basic pattern in a different way to solve a different musical problem. All three share the same first five degrees and differ only in degrees 6 and 7.

**Natural minor.** Step pattern: [2, 1, 2, 2, 1, 2, 2]. Seven notes, summing to 12. Compare this to the major scale pattern [2, 2, 1, 2, 2, 2, 1]. The natural minor is a rotation: take the major scale pattern and start reading from the sixth position. The major pattern, shifted, becomes 2, 1, 2, 2, 1, 2, 2. This connection to rotations will be the central topic of Part VI (Modes), where the natural minor is identified as the Aeolian mode. For now, the observation is noted and the full treatment deferred.

**Worked Example 23.** Build the natural minor scale on root 9 (A).

Starting at 9, applying [2, 1, 2, 2, 1, 2, 2]:

- 9 + 2 = 11
- 11 + 1 = 0
- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 1 = 5
- 5 + 2 = 7

Scale: {9, 11, 0, 2, 4, 5, 7}. In letter names: A, B, C, D, E, F, G. The same seven pitch classes as C major, but rooted on 9 instead of 0. Same notes, different starting point, profoundly different sound. The root changes which pitch class functions as "home," and this alone transforms the cheerful brightness of C major into the darker, more plaintive character of A minor.

**Harmonic minor.** The natural minor has a gap of 2 semitones between its seventh degree and the root. In C major, the seventh degree (B, pitch class 11) sits just 1 semitone below the root (C, pitch class 0), creating a strong pull toward resolution. In A natural minor, the seventh degree (G, pitch class 7) sits 2 semitones below the root (A, pitch class 9). That wider gap weakens the gravitational pull toward the root. The harmonic minor addresses this by raising the seventh degree by 1 semitone, creating a leading tone that sits just 1 semitone below the root.

Step pattern: [2, 1, 2, 2, 1, 3, 1]. The raised seventh changes the step between degrees 6 and 7 from 2 to 3 (an augmented second, or minor-third-sized step) and the step between degrees 7 and 1 from 2 to 1. This introduces a 3-semitone gap, the largest step in any standard seven-note scale, giving the harmonic minor its distinctive exotic sound.

**Worked Example 24.** Build the harmonic minor scale on root 9 (A).

Starting at 9, applying [2, 1, 2, 2, 1, 3, 1]:

- 9 + 2 = 11
- 11 + 1 = 0
- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 1 = 5
- 5 + 3 = 8
- 8 + 1 = 9 (returns to root, confirming the sum is 12)

Scale: {9, 11, 0, 2, 4, 5, 8}. Compared to the natural minor {9, 11, 0, 2, 4, 5, 7}, only one note has changed: pitch class 8 (G♯) replaces pitch class 7 (G). That single semitone alteration creates the leading tone. The interval from degree 7 (pitch class 8) to the root (pitch class 9) is now 1 semitone, matching the major scale's strong pull toward resolution.

**Melodic minor.** The harmonic minor solves the leading-tone problem but creates a new one: the 3-semitone gap between degrees 6 and 7 is awkward to sing. It sounds like a skip rather than a step, disrupting the smooth, stepwise motion that melodies typically favor. The melodic minor addresses this by also raising degree 6, eliminating the augmented second.

Ascending step pattern: [2, 1, 2, 2, 2, 2, 1]. Both degree 6 and degree 7 are raised. Descending, the melodic minor reverts to the natural minor, lowering both degrees back again: [2, 2, 1, 2, 2, 1, 2] (the natural minor steps in reverse). This asymmetry, different notes ascending and descending, is unique among common scales. It reflects a practical compromise: the raised degrees are needed going up (to approach the root from below with strong melodic pull) but unnecessary going down (where the melody moves away from the root, and the pull is less relevant).

**Worked Example 25.** Build the melodic minor scale on root 9 (A), ascending.

Starting at 9, applying [2, 1, 2, 2, 2, 2, 1]:

- 9 + 2 = 11
- 11 + 1 = 0
- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 2 = 6
- 6 + 2 = 8

Ascending scale: {9, 11, 0, 2, 4, 6, 8}. In letter names: A, B, C, D, E, F♯, G♯. Compared to the natural minor, degrees 6 and 7 are each raised by 1 semitone. Compared to A major {9, 11, 1, 2, 4, 6, 8}, only degree 3 differs: the melodic minor has pitch class 0 (C) where the major has pitch class 1 (C♯). The ascending melodic minor is, in a sense, a major scale with a lowered third.

Descending, the melodic minor reverts: {9, 7, 5, 4, 2, 0, 11, 9}. This is simply the natural minor descending. The scale changes shape depending on direction, a feature that the step-pattern formalism handles naturally by specifying separate ascending and descending patterns.

The melodic minor's asymmetry is unusual but not arbitrary. It encodes a practical rule: when approaching the root from below, raise the 6th and 7th degrees to create smooth stepwise motion and a strong leading tone. When descending away from the root, the pull is unnecessary, so the degrees revert. In jazz, however, the ascending form is often used in both directions, treated as a fixed scale rather than a directional one. In that context it is sometimes called the "jazz minor," and its step pattern [2, 1, 2, 2, 2, 2, 1] applies regardless of direction. The same pitch classes, the same arithmetic, but a different convention about when to apply it.

## III.D. Pentatonic and Blues Scales

Not every scale uses seven notes. The pentatonic scales use five, and their simplicity gives them a distinctive open quality found in folk music worldwide, from Scottish ballads to Chinese classical music to West African vocal traditions.

**Major pentatonic.** Step pattern: [2, 2, 3, 2, 3]. Five notes, summing to 12. The wider steps (3 semitones each) create spaciousness. No interval between adjacent scale degrees is as small as 1 semitone, which means the scale contains no half-step tension. Everything sounds consonant against everything else, a property that makes pentatonic scales forgiving and versatile.

**Worked Example 26.** Build the major pentatonic on root 0 (C).

Starting at 0, applying [2, 2, 3, 2, 3]:

- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 3 = 7
- 7 + 2 = 9

Scale: {0, 2, 4, 7, 9}. In letter names: C, D, E, G, A. This is the C major scale with degrees 4 and 7 removed (pitch classes 5 and 11, the notes F and B). These two omitted notes are precisely the ones that sit just 1 semitone from a neighbor in the major scale: F is 1 semitone above E, and B is 1 semitone below C. Removing them eliminates all half-step adjacencies.

**Minor pentatonic.** Step pattern: [3, 2, 2, 3, 2]. Five notes, same total.

**Worked Example 27.** Build the minor pentatonic on root 9 (A).

Starting at 9, applying [3, 2, 2, 3, 2]:

- 9 + 3 = 0
- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 3 = 7

Scale: {9, 0, 2, 4, 7}. In letter names: A, C, D, E, G. These are the same five pitch classes as the C major pentatonic, mirroring the relationship between C major and A natural minor. The relative minor pentatonic contains exactly the same notes as its relative major pentatonic, rooted 3 semitones lower.

**Blues scale.** The blues scale takes the minor pentatonic and adds one note: the "blue note," which is the tritone above the root (6 semitones). This addition injects a concentrated dose of dissonance into an otherwise consonant framework.

**Worked Example 28.** Build the blues scale on root 9 (A).

Start with the A minor pentatonic {9, 0, 2, 4, 7}. Add the blue note: (9 + 6) mod 12 = 3. Insert it in order.

Scale: {9, 0, 2, 3, 4, 7}. Step pattern: [3, 2, 1, 1, 3, 2]. Six notes. In letter names: A, C, D, D♯/E♭, E, G. The blue note (pitch class 3, which traditional notation calls D♯ or E♭ in this context) sits between the minor third (D, pitch class 2) and the major third (E, pitch class 4) of the root. This chromatic cluster of three consecutive semitones (2, 3, 4) creates the characteristic tension of the blues: the melody hovers between minor and major, never fully committing to either, bending between sadness and defiance.

The step pattern [3, 2, 1, 1, 3, 2] contains two steps of 1 semitone, which the pentatonic scales carefully avoid. The blues scale reintroduces half-step tension deliberately, in a specific location, for expressive purpose. The dissonance is not a flaw. It is the point.

In practice, blues musicians rarely play the blue note as a fixed pitch. On guitar, the string is bent; on saxophone, the embouchure shifts; vocalists slide through the pitch rather than landing squarely on it. The blue note lives in the crack between the minor and major third, occupying a region of pitch space that equal temperament does not have a single key for. The blues scale as notated here, with pitch class 3 as a discrete element, is an approximation of something more fluid. But the approximation captures the essential structural fact: the blues introduces chromatic tension into a pentatonic frame.

## III.E. Chromatic and Whole-Tone Scales

At the extremes of scale construction sit two symmetric scales, each interesting for what it lacks.

**The chromatic scale** includes all twelve pitch classes. Its step pattern is [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]. Every semitone is present. There is no hierarchy among the notes, no sense of "home," no pull toward resolution. The chromatic scale is the raw material from which all other scales are carved. Playing it ascending or descending produces a smooth, featureless glide, each note flowing into the next with equal weight. It is to scales what white light is to color: the undifferentiated whole.

Because the chromatic scale contains every pitch class, transposing it is a null operation. Starting from pitch class 0 or pitch class 5 or any other root produces the same set of twelve pitch classes. There is only one chromatic scale. This makes it unique among scales: every other scale in this chapter has multiple transpositions, each selecting a different subset of Z₁₂. The chromatic scale selects all of Z₁₂, leaving nothing out and therefore leaving nowhere to transpose to.

**The whole-tone scale** moves in the opposite direction from the chromatic, using the widest possible equal step. Its pattern is [2, 2, 2, 2, 2, 2]. Six notes, each separated by 2 semitones (a whole step), summing to 12.

**Worked Example 29.** Build the whole-tone scale on root 0.

Starting at 0, applying [2, 2, 2, 2, 2, 2]:

- 0 + 2 = 2
- 2 + 2 = 4
- 4 + 2 = 6
- 6 + 2 = 8
- 8 + 2 = 10

Scale: {0, 2, 4, 6, 8, 10}. Now try root 2: {2, 4, 6, 8, 10, 0}. The same six pitch classes. Root 4: {4, 6, 8, 10, 0, 2}. Still the same six pitch classes. Every even pitch class produces the same set. This means that transposing the whole-tone scale by 2 semitones maps it onto itself.

Now try root 1: {1, 3, 5, 7, 9, 11}. This is a different set, containing all the odd pitch classes. Root 3: {3, 5, 7, 9, 11, 1}. Same set again. There are exactly two distinct whole-tone scales. One contains the even pitch classes, the other the odd ones. Together they partition Z₁₂ into two non-overlapping halves.

The whole-tone scale's perfect symmetry gives it a floating, dreamlike quality. Because every step is the same size, no note feels more stable than any other. There is no leading tone pulling toward resolution, no perfect fifth anchoring a tonal center. Debussy used whole-tone scales extensively, and the sound is immediately recognizable: shimmering, suspended, directionless. The scale's lack of internal contrast is both its defining feature and its limitation. Extended passages in whole-tone harmony can feel static, because the ear has no asymmetry to latch onto.

**The octatonic scale** (also called the diminished scale) alternates two step sizes. The two variants are [2, 1, 2, 1, 2, 1, 2, 1] (whole-half) and [1, 2, 1, 2, 1, 2, 1, 2] (half-whole). Eight notes, summing to 12.

**Worked Example 30.** Build the whole-half octatonic scale on root 0.

Starting at 0, applying [2, 1, 2, 1, 2, 1, 2, 1]:

- 0, 2, 3, 5, 6, 8, 9, 11

Eight pitch classes out of twelve. Now try root 3: starting at 3, applying the same pattern gives {3, 5, 6, 8, 9, 11, 0, 2}. The same eight pitch classes in a different order. The octatonic scale maps onto itself under transposition by 3 semitones.

Since the pattern repeats every 3 semitones and 12/3 = 4, there are exactly three distinct octatonic scales:

- {0, 1, 3, 4, 6, 7, 9, 10} (starting from root 0 with half-whole, or root 1 with whole-half)
- {0, 2, 3, 5, 6, 8, 9, 11} (as computed above)
- {1, 2, 4, 5, 7, 8, 10, 11}

A pattern emerges across these symmetric scales. The chromatic scale, with step size 1, maps onto itself under any transposition: one distinct version. The whole-tone scale, with step size 2, maps onto itself under transposition by 2: two distinct versions. The octatonic scale, with a pattern repeating every 3 semitones, maps onto itself under transposition by 3: three distinct versions. The more internal symmetry a scale possesses, the fewer distinct transpositions it admits.[^18] This is a consequence of the group structure of Z₁₂: a scale that is invariant under a subgroup of transpositions has as many distinct versions as the index of that subgroup. The connection to group theory will not be developed formally here, but the pattern itself is worth noticing: symmetry reduces variety.

## III.F. Scale Comparison by Interval Content

The interval vector, introduced in Section II.F, provides a way to compare scales by their total intervallic content rather than by their specific pitch classes. Two scales with the same interval vector share the same distribution of intervallic relationships, even if they contain different notes and sound different in context.

Computing the interval vector for a seven-note scale requires tallying all 7(6)/2 = 21 pairs. For brevity, the results are presented directly, with the reader invited to verify any entry.

**The major scale** {0, 2, 4, 5, 7, 9, 11}:

| IC | Pairs | Count |
|:--:|:------|:-----:|
| 1  | 0-11, 4-5 | 2 |
| 2  | 0-2, 2-4, 5-7, 7-9, 9-11 | 5 |
| 3  | 0-9, 2-5, 2-11, 4-7 | 4 |[^19]
| 4  | 0-4, 5-9, 7-11 | 3 |
| 5  | 0-5, 0-7, 2-7, 2-9, 4-9, 4-11 | 6 |
| 6  | 5-11 | 1 |

Interval vector: [2, 5, 4, 3, 6, 1]. Notice several features. IC 5 (the perfect fifth/fourth) is the most abundant, with 6 instances. This makes the major scale rich in the most consonant non-octave interval, contributing to its stable, grounded quality. IC 1 (the semitone) appears only twice, providing just enough half-step tension for melodic leading tones without overwhelming the scale's consonance. IC 6 (the tritone) appears exactly once, creating a single point of acute dissonance, the famous tritone between degrees 4 and 7 that drives dominant-to-tonic resolution. Every interval class is represented at least once. The major scale is, in a precise sense, maximally diverse.[^20]

**The harmonic minor scale** {0, 2, 3, 5, 7, 8, 11} (transposed to root 0 for comparison):

Interval vector: [3, 3, 5, 4, 4, 2]. Compared to the major scale's [2, 5, 4, 3, 6, 1], the harmonic minor has more semitone pairs (3 vs. 2) and fewer perfect fifths (4 vs. 6). It also has more minor thirds (5 vs. 4) and an additional tritone (2 vs. 1). The increase in semitone content reflects the additional half-step relationships introduced by the raised seventh. The decrease in perfect fifths corresponds to the harmonic minor's less purely diatonic character. The extra tritone contributes to the scale's heightened tension and its usefulness in creating strong dominant-to-tonic resolutions.

**The whole-tone scale** {0, 2, 4, 6, 8, 10}:

Six notes yield 6(5)/2 = 15 pairs. Interval vector: [0, 6, 0, 6, 0, 3]. The zeros are striking: no semitones (IC 1), no minor thirds (IC 3), no perfect fifths (IC 5). The scale contains only whole tones (IC 2), major thirds (IC 4), and tritones (IC 6). This extreme lopsidedness explains the whole-tone scale's unique sound. The absence of perfect fifths means no stable anchoring. The absence of semitones means no leading-tone pull. The abundance of tritones means pervasive, evenly distributed tension. The interval vector makes audible character visible as numerical structure.

**The octatonic scale** {0, 1, 3, 4, 6, 7, 9, 10}:

Eight notes yield 8(7)/2 = 28 pairs. Interval vector: [4, 4, 8, 4, 4, 4]. Nearly uniform, with IC 3 (the minor third) doubly represented. The octatonic scale comes closer than any other common scale to distributing its intervals evenly, giving it a quality of balanced tension, neither as grounded as the major scale nor as floating as the whole-tone.

Comparing the four vectors side by side:

| Scale | [IC1, IC2, IC3, IC4, IC5, IC6] | Total pairs |
|:------|:---:|:---:|
| Major | [2, 5, 4, 3, 6, 1] | 21 |
| Harmonic minor | [3, 3, 5, 4, 4, 2] | 21 |
| Whole-tone | [0, 6, 0, 6, 0, 3] | 15 |
| Octatonic | [4, 4, 8, 4, 4, 4] | 28 |

The vector is a fingerprint. No two of these scales share the same distribution, and the differences in distribution correspond directly to differences in sound. The major scale's dominance of IC 5 makes it consonant and stable. The whole-tone scale's missing intervals make it ethereal. The octatonic scale's near-uniformity makes it tense but balanced.

The comparison also reveals something about scale design. The major scale is the only common seven-note scale whose interval vector contains all six interval classes, with IC 5 (the perfect fifth) most prominent and IC 6 (the tritone) least prominent. This distribution gives it maximum intervallic variety weighted toward consonance: many fifths and fourths for stability, a moderate number of thirds for color, just enough semitones for melodic tension, and a single tritone for harmonic drive. The harmonic minor, by contrast, trades some of that fifth-heavy consonance for additional semitone tension, which is precisely why it sounds more angular and dramatic.

The whole-tone vector [0, 6, 0, 6, 0, 3] is remarkable for its zeros. Three of the six interval classes are entirely absent. A composer writing in the whole-tone scale simply cannot produce a perfect fifth, a minor third, or a semitone. These are not difficult to find or rare. They do not exist in the vocabulary. The sonic result is a scale that sounds fundamentally unlike any diatonic scale, because the intervals that define diatonic music (the fifth, the half step) are structurally impossible.

The interval vector does not capture everything about a scale's character. The ordering of notes matters, and so does the root. Two scales with identical vectors can still sound different in musical context, because which specific pitch classes participate affects key relationships and voice leading. But the vector captures more than any single number could. It translates the vague notion of "this scale sounds different from that scale" into a precise, comparable list of quantities. When two scales share a vector, they share an intervallic palette. When they differ, the difference is quantified, and the quantification often explains the perceptual contrast.

# Part IV: KEYS AND KEY SIGNATURES

A scale is a collection of pitch classes selected by a step pattern. A key is something more. It takes that collection and declares one of its members the center of gravity, the point of rest, the PC that all the others orbit. Everything in tonal music depends on that declaration.

## IV.A. Keys as Rooted Scales

A key is a pair: (tonic, scale type). The tonic is a pitch class in Z₁₂. The scale type determines a step pattern. Together they produce a set of pitch classes and an assertion about which one matters most.

The key of (0, major) means: tonic = 0, scale type = major, step pattern = [2, 2, 1, 2, 2, 2, 1]. Applying that pattern from 0 gives the pitch-class set {0, 2, 4, 5, 7, 9, 11}. Any melody or harmony operating within this key treats PC 0 as home. Music in the key of (0, major) tends to begin on or near PC 0, departs from it to create tension, and returns to it for resolution. The pitch-class set tells you which notes are available. The tonic tells you what they mean.

The key signature is the set of pitch classes belonging to the key's scale. For (0, major), the key signature is {0, 2, 4, 5, 7, 9, 11}. For (7, major), it is {7, 9, 11, 0, 2, 4, 6}. The key signature says nothing about hierarchy. It is a pure set, unordered, with no distinguished element. Two musicians can look at the same key signature and be playing in different keys.

This happens when two keys share the same PC set but differ in tonic. The key of (0, major) uses {0, 2, 4, 5, 7, 9, 11}. The key of (9, natural minor) uses step pattern [2, 1, 2, 2, 1, 2, 2] from root 9, producing {9, 11, 0, 2, 4, 5, 7}. Written as sets, these are identical. The seven pitch classes are the same. But music in (0, major) gravitates toward PC 0, while music in (9, minor) gravitates toward PC 9. These are called relative keys: same key signature, different tonic.

The tonic is not the only PC with a special role. In any major or minor key, the pitch class 7 semitones above the tonic is the dominant. In (0, major), the dominant is PC 7. In (5, major), the dominant is (5 + 7) mod 12 = 0. The dominant is the second most stable pitch class, the one that most urgently wants to resolve to the tonic. The relationship between tonic and dominant will drive chord progressions in later parts. For now, the point is that a key is not just a bag of notes. It is a bag of notes with a hierarchy, and the tonic sits at the top.[^21]

Beyond the tonic and dominant, other scale degrees carry their own tendencies. The fourth degree (5 semitones above the tonic) pulls downward toward the third. The seventh degree (11 semitones above the tonic, in major) pulls sharply upward toward the tonic, so strongly that it is called the leading tone. These tendencies are not properties of the pitch classes themselves. PC 11 has no inherent urge to go anywhere. The pull exists only within the context of a key, where PC 11 sits one semitone below the tonic PC 0 and the listener's ear expects the gap to close. A key, then, is a pitch-class set plus a web of expectations.

In the integer system, transposing to a new key requires changing a single parameter. The step pattern for all major keys is the same: [2, 2, 1, 2, 2, 2, 1]. The step pattern for all natural minor keys is the same: [2, 1, 2, 2, 1, 2, 2]. To move from the key of (0, major) to the key of (3, major), you change the tonic from 0 to 3 and recompute: {3, 5, 7, 8, 10, 0, 2}. The pattern is invariant. Only the starting point changes. This is a direct consequence of building on mod 12 arithmetic rather than letter names. There is no need to reason about "three flats" or "E♭ major." The key is (3, major), and its PC set follows mechanically.

Traditional theory often presents each key as a separate entity to be studied individually: "the key of E♭ major has three flats, B♭, E♭, and A♭." In the integer framework, there is nothing individual to study. Every major key is the same structure, relocated. The key of (3, major) differs from the key of (0, major) only in its starting position on the Z₁₂ clock. Everything else, the intervals between adjacent scale degrees, the relationship of dominant to tonic, the size of each step, is preserved exactly. This is what mathematicians mean by translation invariance, and it is built into the system by construction.

## IV.B. Sharps, Flats, and the Spelling Convention

Traditional notation uses sharps and flats in key signatures to mark which pitch classes deviate from the default set. The default is C major: {0, 2, 4, 5, 7, 9, 11}, the set that uses all naturals and no sharps or flats. Every other major key is described by how many and which PCs it alters from that baseline.

In our system, this layer of description is unnecessary. A key signature is a set of seven pitch classes, and no set is more "default" than any other. The set {0, 2, 4, 5, 7, 9, 11} has no special algebraic status. It happens to be the major scale built on PC 0, which traditional notation calls C, but there is nothing about the integer 0 that privileges it over any other tonic. The sharp and flat system is a historical artifact of building notation around one particular key.

That said, the sharp/flat system encodes a real pattern worth understanding. Each sharp added to a key signature corresponds to one clockwise step on the circle of fifths (which we will construct in Part V). Each flat corresponds to one counterclockwise step. The pattern is orderly:

The order of sharps, expressed as pitch classes: 6, 1, 8, 3, 10, 5, 0. In letter names: F♯, C♯, G♯, D♯, A♯, E♯, B♯. Each new sharp enters the key signature at a predictable position.

The order of flats reverses this: 10, 3, 8, 1, 6, 11, 4. In letter names: B♭, E♭, A♭, D♭, G♭, C♭, F♭.

The following table shows how key signatures accumulate sharps or flats, listing the major key tonic and the resulting PC set:

| Sharps/Flats | Major tonic | PC set |
|:---:|:---:|:---|
| 0 | 0 | {0, 2, 4, 5, 7, 9, 11} |
| 1♯ | 7 | {0, 2, 4, 6, 7, 9, 11} |
| 2♯ | 2 | {1, 2, 4, 6, 7, 9, 11} |
| 3♯ | 9 | {1, 2, 4, 6, 8, 9, 11} |
| 4♯ | 4 | {1, 3, 4, 6, 8, 9, 11} |
| 5♯ | 11 | {1, 3, 4, 6, 8, 10, 11} |
| 6♯ | 6 | {1, 3, 5, 6, 8, 10, 11} |
| 1♭ | 5 | {0, 2, 4, 5, 7, 9, 10} |
| 2♭ | 10 | {0, 2, 3, 5, 7, 9, 10} |
| 3♭ | 3 | {0, 2, 3, 5, 7, 8, 10} |
| 4♭ | 8 | {0, 1, 3, 5, 7, 8, 10} |
| 5♭ | 1 | {0, 1, 3, 5, 6, 8, 10} |
| 6♭ | 6 | {1, 3, 5, 6, 8, 10, 11} |

Notice that the tonic of each sharp key is 7 more than the previous (mod 12): 0, 7, 2, 9, 4, 11, 6. Each flat key's tonic is 5 more than the previous: 0, 5, 10, 3, 8, 1, 6. Both sequences arrive at tonic 6 after six steps.

There is an elegant arithmetic behind each step. Moving from one sharp key to the next, you add PC (previous tonic + 6) mod 12 and remove PC (previous tonic + 5) mod 12.[^22] Going from 0 sharps (tonic 0) to 1 sharp (tonic 7): add (0 + 6) mod 12 = 6, remove (0 + 5) mod 12 = 5. Check the table: {0, 2, 4, 5, 7, 9, 11} loses 5 and gains 6 to become {0, 2, 4, 6, 7, 9, 11}. Going from 1 sharp to 2 sharps: add (7 + 6) mod 12 = 1, remove (7 + 5) mod 12 = 0. The set loses 0 and gains 1. The pattern holds at every step.

**Worked Example 31.** Start from 3 sharps, tonic 9, PC set {1, 2, 4, 6, 8, 9, 11}. Predict the 4-sharp key. New tonic: (9 + 7) mod 12 = 4. Add PC (9 + 6) mod 12 = 3. Remove PC (9 + 5) mod 12 = 2. New set: {1, 3, 4, 6, 8, 9, 11}. Check: this is the major scale from root 4 with step pattern [2, 2, 1, 2, 2, 2, 1], giving 4, 6, 8, 9, 11, 1, 3. Confirmed.

## IV.C. Enharmonic Equivalence

In equal temperament, every pitch class has one and only one frequency (within a given octave). PC 6 has a frequency. It does not have two frequencies depending on whether you call it F♯ or G♭. The letter names F♯ and G♭ are two labels for the same point in Z₁₂.

This is enharmonic equivalence: distinct letter-name spellings that refer to the same pitch class. In the integer system, the concept barely needs a name. PC 6 is PC 6. There is nothing to "equivalence" because there is nothing to distinguish. The ambiguity exists only in the letter-name layer, and we have removed that layer from the foundations.

Traditional notation cares deeply about the distinction. In the key of (2, major), the pitch class 6 is spelled F♯, because the key has two sharps and F♯ is one of them. In the key of (6, major) spelled with flats (as G♭ major), the same pitch class 6 is spelled G♭. A musician reading sheet music needs to know which spelling to expect, because it affects which line or space the note sits on. But the sound is identical. The distinction is about visual layout on the staff, not about acoustics or music theory.

Enharmonic equivalence creates what traditional theory calls enharmonic keys. The key of (6, major) can be spelled with 6 sharps (F♯ major) or 6 flats (G♭ major). Both spellings produce the same PC set: {1, 3, 5, 6, 8, 10, 11}.[^23] In traditional notation, these two spellings produce different key signatures on the staff, with different accidentals, even though a pianist presses the same keys for both. Similarly, 5 sharps (tonic 11, B major) and 7 flats (tonic 11, C♭ major) would refer to the same pitch classes.

Consider another case. The key of (1, major) can be spelled as D♭ major (5 flats) or as C♯ major (7 sharps). Seven sharps means every note in the scale is sharped, which traditional notation handles but finds cumbersome. Most publishers choose D♭ major. The choice is purely typographical. In the integer system, the key is (1, major), its PC set is {1, 3, 5, 6, 8, 10, 0}, and there is no decision to make.

The entire apparatus of enharmonic equivalence, the long explanations in traditional textbooks, the careful distinctions between "sharp keys" and "flat keys," the rules about when to respell, dissolves in the integer system. It dissolves because the apparatus was never about sound. It was about managing the mismatch between a seven-letter naming system and a twelve-pitch reality. Remove the seven letters, and the mismatch vanishes.

**Worked Example 32.** A traditional textbook asks: "Is D♯ major a real key?" In letter-name theory, D♯ major would require a double sharp in its key signature (F𝄪), making it unconventional. In the integer system: D♯ = PC 3. The key of (3, major) = {3, 5, 7, 8, 10, 0, 2}. It is as "real" as any other major key. The question was never about the key. It was about the limits of letter-name spelling.

## IV.D. Relative and Parallel Keys

Two keys can be related by sharing pitch classes (same key signature, different tonic) or by sharing a tonic (same home, different scale type). The first relationship is called relative. The second is called parallel.

Relative keys share a key signature. Every major key has a relative minor, and every minor key has a relative major. The relationship is arithmetic. Given a major key with tonic t, its relative minor has tonic (t + 9) mod 12, which is the same as (t - 3) mod 12. Given a minor key with tonic t, its relative major has tonic (t + 3) mod 12.

The number 9 (or equivalently, -3 mod 12) is not arbitrary. The natural minor scale's step pattern [2, 1, 2, 2, 1, 2, 2] is the major scale's step pattern [2, 2, 1, 2, 2, 2, 1] started from its sixth degree. The sixth degree of a major scale built on t is reached by applying steps 2 + 2 + 1 + 2 + 2 = 9. So the minor tonic sits 9 semitones above the major tonic.[^24]

**Worked Example 33.** Key of (7, major) = {7, 9, 11, 0, 2, 4, 6}. Relative minor tonic: (7 + 9) mod 12 = 4. Key of (4, natural minor), step pattern [2, 1, 2, 2, 1, 2, 2] from 4: 4, 6, 7, 9, 11, 0, 2, giving the set {4, 6, 7, 9, 11, 0, 2}. This is the same set as {7, 9, 11, 0, 2, 4, 6}. Confirmed: same seven pitch classes, different tonic. In traditional terms, G major and E minor are relative keys.

Parallel keys share a tonic but differ in scale type. The key of (5, major) and the key of (5, minor) both treat PC 5 as home, but they use different pitch classes to build around it.

**Worked Example 34.** Key of (5, major): step pattern [2, 2, 1, 2, 2, 2, 1] from 5 gives 5, 7, 9, 10, 0, 2, 4. PC set: {5, 7, 9, 10, 0, 2, 4}. Key of (5, natural minor): step pattern [2, 1, 2, 2, 1, 2, 2] from 5 gives 5, 7, 8, 10, 0, 1, 3. PC set: {5, 7, 8, 10, 0, 1, 3}. The shared PCs are {5, 7, 10, 0}, four in common. The PCs unique to (5, major) are {9, 2, 4}. The PCs unique to (5, minor) are {8, 1, 3}. Three PCs differ, four PCs overlap.

This count is always the same. Parallel major and minor keys differ in exactly 3 pitch classes out of 7, regardless of the tonic. The reason is structural: comparing the major step pattern [2, 2, 1, 2, 2, 2, 1] with the natural minor [2, 1, 2, 2, 1, 2, 2], the cumulative sums from any shared tonic will agree at positions 0, 1, 4, and 5 (producing four shared PCs) and diverge at positions 2, 3, and 6 (producing three differing PCs).[^25]

The following table lists all 12 major keys with their relative minor tonics and parallel minor tonics:

| Major tonic | Major PC set | Relative minor tonic | Parallel minor tonic |
|:---:|:---|:---:|:---:|
| 0 | {0, 2, 4, 5, 7, 9, 11} | 9 | 0 |
| 1 | {1, 3, 5, 6, 8, 10, 0} | 10 | 1 |
| 2 | {2, 4, 6, 7, 9, 11, 1} | 11 | 2 |
| 3 | {3, 5, 7, 8, 10, 0, 2} | 0 | 3 |
| 4 | {4, 6, 8, 9, 11, 1, 3} | 1 | 4 |
| 5 | {5, 7, 9, 10, 0, 2, 4} | 2 | 5 |
| 6 | {6, 8, 10, 11, 1, 3, 5} | 3 | 6 |
| 7 | {7, 9, 11, 0, 2, 4, 6} | 4 | 7 |
| 8 | {8, 10, 0, 1, 3, 5, 7} | 5 | 8 |
| 9 | {9, 11, 1, 2, 4, 6, 8} | 6 | 9 |
| 10 | {10, 0, 2, 3, 5, 7, 9} | 7 | 10 |
| 11 | {11, 1, 3, 4, 6, 8, 10} | 8 | 11 |

The relative minor tonic is always (major tonic + 9) mod 12. The parallel minor tonic is always the same as the major tonic, by definition. The table may look trivially simple, and that is exactly the point. In the integer system, relationships that fill pages of traditional explanation reduce to one line of arithmetic.

One practical consequence: when you hear a piece and want to know whether it is in a major key or its relative minor, the pitch-class content alone will not tell you. Both keys use the same seven PCs. You have to listen for which PC the music treats as home. Does the melody tend to rest on PC 0, or on PC 9? Does the harmony resolve toward a chord built on PC 0 or on PC 9? The answer determines the key. The set determines the signature, but only the ear determines the tonic.

# Part V: THE CIRCLE OF FIFTHS

The previous four parts built the machinery: pitch classes in Z₁₂, intervals as mod 12 subtraction, scales from step patterns, keys as rooted scales. All of it has been local, focused on individual keys and intervals. Now comes a structure that is global, a single diagram that organizes all twelve keys, all key signatures, and the relationships among them. It emerges from the simplest possible operation: adding 7, over and over.

## V.A. Generating Z₁₂ by Repeated Addition of 7

Start at 0. Add 7. You get 7. Add 7 again: (7 + 7) mod 12 = 2. Again: (2 + 7) mod 12 = 9. Continue:

0 → 7 → 2 → 9 → 4 → 11 → 6 → 1 → 8 → 3 → 10 → 5 → (0)

Count the distinct values: 0, 7, 2, 9, 4, 11, 6, 1, 8, 3, 10, 5. Twelve pitch classes, every element of Z₁₂, visited exactly once before the sequence returns to its starting point. The orbit is complete.

This works because 7 and 12 are coprime: gcd(7, 12) = 1.[^26] When the step size shares no common factor with the modulus, repeated addition must cycle through every element before returning to the start. If the step size shared a factor with 12, the orbit would be shorter. Adding 6 repeatedly from 0 gives 0, 6, 0, 6, ... , an orbit of length 2, because gcd(6, 12) = 6. Adding 4 gives 0, 4, 8, 0, 4, 8, ... , an orbit of length 3, because gcd(4, 12) = 4. Only step sizes coprime to 12 produce full orbits of length 12.

In the language of group theory, the map T₇: p → (p + 7) mod 12 is a permutation of Z₁₂. Applied repeatedly, it generates every element of the group. Its order is 12, meaning you must apply it 12 times before returning to the identity. Any element that generates all of Z₁₂ this way is called a generator of the cyclic group. The integer 7 is one such generator.[^27]

Now arrange these twelve pitch classes in the order the sequence visits them, equally spaced around a circle. Place 0 at the top (twelve o'clock). Moving clockwise, the next position is 7, then 2, then 9, and so on. The result is the circle of fifths.

The name comes from traditional interval naming: 7 semitones is a perfect fifth. Each clockwise step on the circle moves up by a perfect fifth. In our integer system, we might call it the circle of sevens, or the T₇ orbit diagram. The traditional name is so deeply established that we will keep it, with the understanding that "fifth" means "interval of 7 semitones."

**Worked Example 35.** Verify three consecutive steps. Start at PC 4 on the circle. One clockwise step: (4 + 7) mod 12 = 11. Another: (11 + 7) mod 12 = 6. Another: (6 + 7) mod 12 = 1. Check against the full sequence above: ... 4, 11, 6, 1 ... . Confirmed.

The starting point of the sequence is arbitrary. Begin at PC 3 instead of 0 and add 7 repeatedly: 3, 10, 5, 0, 7, 2, 9, 4, 11, 6, 1, 8, (3). All twelve PCs appear again. The orbit is the same cycle, entered at a different point. This is a general property of cyclic permutations: the orbit does not depend on where you start, only on the step size. Any pitch class can serve as the "top" of the circle, though convention places 0 (C) there.

Why 7, specifically? The number 7 is not the only generator of Z₁₂. As we will see in Section 5.D, the integers 1, 5, 7, and 11 all generate the full group. But 7 has a musical distinction: it is the number of semitones in a perfect fifth, the most consonant interval after the octave. Building the circle from 7 means that adjacent positions are related by the strongest harmonic bond available. The circle of fifths is not merely a valid way to arrange the twelve pitch classes. It is the arrangement that reflects harmonic proximity most faithfully.

The circle of fifths is not a new mathematical object. It is a repackaging of Z₁₂ arithmetic into a visual layout optimized for musical insight. Every property of the circle follows from properties of modular addition that we already established.

## V.B. The Circle as a Graph

The twelve pitch classes on the circle, reading clockwise from the top:

```
           0
       5       7
    10             2

    3              9
       8       4
          6
```

With traditional letter correspondences: 0 = C at the top, then clockwise: 7 = G, 2 = D, 9 = A, 4 = E, 11 = B, 6 = F♯/G♭ at the bottom, then continuing: 1 = D♭, 8 = A♭, 3 = E♭, 10 = B♭, 5 = F, back to 0 = C.

Each clockwise step adds 7. Each counterclockwise step adds 5, since (p + 5) mod 12 is the same as moving one position counterclockwise. This is because 5 + 7 = 12 ≡ 0 (mod 12). Moving clockwise by 7 and counterclockwise by 5 land on the same neighbor, approached from opposite directions.

This means the circle of fourths is the same circle traversed counterclockwise. The interval of 5 semitones (traditionally called a perfect fourth) is the complement of 7 (since 5 + 7 = 12). Going up a fifth from any PC is the same as going down a fourth, and vice versa. The two circles are not two structures but one structure read in two directions.[^28]

Think of the circle as a graph with 12 vertices and 12 edges, each edge connecting a PC to its clockwise neighbor. The graph is a single cycle: following edges clockwise from any vertex returns you to the start after exactly 12 steps. In graph-theoretic terms, this is a Hamiltonian cycle on the complete graph of Z₁₂, chosen so that every edge represents the interval 7. Other Hamiltonian cycles exist (using step sizes 1, 5, or 11), but this one aligns with musical structure.

The symmetry goes deeper. The pitch class directly opposite any point on the circle is exactly 6 steps away, reachable by six clockwise jumps of 7, which totals 42 ≡ 6 (mod 12). So the point diametrically opposite PC 0 is PC 6. Opposite PC 7 is PC 1. Opposite PC 2 is PC 8. Each diameter of the circle connects two pitch classes separated by a tritone (6 semitones). The six diameters carve the circle into six pairs: {0, 6}, {7, 1}, {2, 8}, {9, 3}, {4, 10}, {11, 5}. These pairs will reappear when we discuss tritone substitution in the context of chord progressions.

## V.C. Key Signatures on the Circle

The circle's deepest musical utility is the relationship it reveals among key signatures. Adjacent keys on the circle differ by exactly one pitch class in their key signatures. No other arrangement of the twelve keys has this property.

Start at the top with (0, major), PC set {0, 2, 4, 5, 7, 9, 11}. Move one step clockwise to (7, major), PC set {0, 2, 4, 6, 7, 9, 11}. Compare: {0, 2, 4, 5, 7, 9, 11} versus {0, 2, 4, 6, 7, 9, 11}. The first set contains 5 where the second contains 6. One PC differs. This is what "one sharp" means: the key of (7, major) has one sharp relative to (0, major), and that sharp is PC 6 (traditionally F♯), replacing PC 5 (traditionally F).

Each additional clockwise step adds one sharp (or, equivalently, removes one flat). Each counterclockwise step adds one flat (or removes one sharp). The number of steps between two keys on the circle equals the number of pitch classes by which their key signatures differ.

**Worked Example 36.** How many PCs differ between (0, major) and (2, major)? The key of (2, major) is 2 clockwise steps from (0, major) on the circle: 0 → 7 → 2. So the signatures should differ by 2 PCs. Check: (0, major) = {0, 2, 4, 5, 7, 9, 11}. (2, major) = {1, 2, 4, 6, 7, 9, 11}. The set {0, major} has PCs 0 and 5; the set (2, major) has PCs 1 and 6 instead. Exactly 2 PCs differ. Confirmed.

**Worked Example 37.** How many PCs differ between (0, major) and (8, major)? Count clockwise steps from 0 to 8 on the circle: 0 → 7 → 2 → 9 → 4 → 11 → 6 → 1 → 8, that is 8 steps. But the circle has 12 positions, so the shorter path might be counterclockwise: 0 → 5 → 10 → 3 → 8, which is 4 steps. The number of differing PCs is the shorter of the two distances, so 4. Verify: (0, major) = {0, 2, 4, 5, 7, 9, 11}. (8, major) = {8, 10, 0, 1, 3, 5, 7}. Shared PCs: {0, 5, 7}. PCs in (0, major) only: {2, 4, 9, 11}. PCs in (8, major) only: {8, 10, 1, 3}. Four PCs differ. Confirmed.

This makes the circle of fifths a map of harmonic proximity. Keys that are close together on the circle share most of their pitch classes and sound closely related. Keys on opposite sides share the fewest pitch classes and sound maximally distant. A listener will perceive a shift from (0, major) to (7, major) as gentle (only one new note) and a shift from (0, major) to (6, major) as dramatic (six new notes).[^29]

The order of sharps and flats, introduced in Section 4.B, follows the circle directly. The sharps accumulate in the order you encounter them moving clockwise: PC 6 (first sharp), PC 1 (second), PC 8 (third), PC 3 (fourth), PC 10 (fifth), PC 5 (sixth). These are the PCs that enter the key signature, in order, as you walk clockwise. The flats accumulate counterclockwise: PC 10 (first flat), PC 3 (second), PC 8 (third), PC 1 (fourth), PC 6 (fifth), PC 11 (sixth). This is not a separate fact to memorize. It is a direct reading of the circle.

## V.D. Tritone Symmetry

The pitch classes at opposite ends of any diameter are 6 semitones apart: a tritone. PC 0 faces PC 6. PC 7 faces PC 1. PC 2 faces PC 8. Six such diameters partition the twelve pitch classes into six pairs.

The keys at opposite points on the circle are maximally distant. The key of (0, major) and the key of (6, major) differ in 6 of their 7 pitch classes, sharing only one PC. Check: (0, major) = {0, 2, 4, 5, 7, 9, 11}. (6, major) = {6, 8, 10, 11, 1, 3, 5}. Shared: {5, 11}. That is actually 2 shared PCs, so 5 differ.[^30] The point stands: opposite keys on the circle are the most harmonically remote. They share the fewest pitch classes of any pair of major keys that are 6 steps apart.

The tritone itself, the interval of 6 semitones, has a unique algebraic property that explains its position. Adding 6 repeatedly from 0: 0, 6, 0, 6, 0, 6, ... . The orbit has length 2, not 12. This is because gcd(6, 12) = 6. The number 6 generates only a subgroup of Z₁₂, specifically the subgroup {0, 6} of order 2.

Contrast this with 7. Adding 7 repeatedly visits all 12 pitch classes. Adding 6 repeatedly visits only 2. The number 7 is a generator of Z₁₂. The number 6 is the worst possible candidate for a generator: it produces the smallest nontrivial subgroup.

This contrast illustrates a foundational result from group theory. An integer k generates Z₁₂ (meaning repeated addition of k visits all 12 elements) if and only if gcd(k, 12) = 1. The generators of Z₁₂ are the integers coprime to 12:

| k | gcd(k, 12) | Orbit length | Generator? |
|:---:|:---:|:---:|:---:|
| 1 | 1 | 12 | Yes |
| 2 | 2 | 6 | No |
| 3 | 3 | 4 | No |
| 4 | 4 | 3 | No |
| 5 | 1 | 12 | Yes |
| 6 | 6 | 2 | No |
| 7 | 1 | 12 | Yes |
| 8 | 4 | 3 | No |
| 9 | 3 | 4 | No |
| 10 | 2 | 6 | No |
| 11 | 1 | 12 | Yes |

Four generators: 1, 5, 7, and 11. In interval terms: the semitone (1), the perfect fourth (5), the perfect fifth (7), and the major seventh (11). Any of these could be used to build a circle visiting all 12 pitch classes. The circle of fifths uses 7 because the perfect fifth is the most consonant interval after the octave and the unison, giving the circle both algebraic completeness and musical naturalness.

**Worked Example 38.** Build the "circle of semitones" by adding 1 repeatedly: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, (0). This visits all 12 PCs (as expected, since gcd(1, 12) = 1), but adjacent keys on this circle differ by up to 5 or 6 PCs. Moving from (0, major) to (1, major) changes 5 pitch classes. The circle of semitones is algebraically valid but musically useless as an organizing tool for key relationships. The circle of fifths wins because adjacent positions differ in only 1 PC.

## V.E. Applications of the Circle

The circle of fifths earns its reputation as the most useful single diagram in tonal music through several applications that later parts will develop in full. Here is a preview of how the circle connects to the territory ahead.

Closely related keys sit 1 or 2 steps apart on the circle. The key of (0, major) is closely related to (7, major), (5, major), (9, minor), (4, minor), and (2, minor), all within 1 or 2 steps. A composer writing in (0, major) who wants to introduce variety without disorienting the listener will move to one of these neighbors. Distant keys, 4, 5, or 6 steps away, create a sense of dramatic contrast or journey.

Modulation, the act of changing key within a piece, most commonly moves to an adjacent key on the circle. A piece in (0, major) might modulate to (7, major) for its middle section and return to (0, major) for its ending. The listener hears this as a subtle brightening: six of the seven pitch classes stay the same, and only one changes. A modulation three steps away (say, from (0, major) to (9, major)) feels more dramatic, because three pitch classes shift at once. Distance on the circle maps directly to the perceptual "cost" of a key change. This will be explored systematically in Part IX.

Chord progressions, the sequences of chords that form the harmonic backbone of a piece, often follow paths on the circle. The most important progression in Western tonal music, the "dominant to tonic" resolution, moves one step counterclockwise: from the chord built on the dominant (scale degree 5, which is PC 7 in the key of 0) to the chord built on the tonic (PC 0). The progression ii, V, I, the backbone of jazz and much classical music, traces two counterclockwise steps: starting from a chord on scale degree 2 (PC 2 in key of 0), moving to scale degree 5 (PC 7), landing on scale degree 1 (PC 0). On the circle, the roots move 2 → 7 → 0, each step counterclockwise. Chord progressions will be the subject of Parts VII and VIII.[^31]

The circle also explains the ordering of sharps and flats in traditional key signatures. The order of sharps, 6, 1, 8, 3, 10, 5, follows the circle clockwise starting from PC 6. The order of flats, 10, 3, 8, 1, 6, 11, follows it counterclockwise starting from PC 10. Traditional musicians memorize these as acronyms. In the integer system, there is nothing to memorize: you read them off the circle.

Finally, the circle provides a distance metric for keys. The circle distance between two major keys with tonics t₁ and t₂ is:

> d(t₁, t₂) = min(n, 12 - n), where n is the number of clockwise steps from t₁ to t₂ on the circle

This distance counts the number of pitch classes that differ between the two key signatures, and it ranges from 0 (same key) to 6 (tritone-related keys, maximally distant).

**Worked Example 39.** Find the circle distance between (9, major) and (3, major). On the circle, 9 sits at position 4 (counting clockwise from 0: 0, 7, 2, 9 is three steps, so position 3). And 3 sits at position 9 (count: 0, 7, 2, 9, 4, 11, 6, 1, 8, 3 is nine steps, so position 9). Clockwise distance from position 3 to position 9 is 6. Counterclockwise distance is 12 - 6 = 6. So d(9, 3) = 6. These are tritone-related keys, maximally distant. Verify: (9, major) = {9, 11, 1, 2, 4, 6, 8} and (3, major) = {3, 5, 7, 8, 10, 0, 2}. Shared PCs: {2, 8}. That is 2 shared, 5 differing. The maximum-distance pair, as expected.

The circle of fifths is, at bottom, a single arithmetic fact rendered visual: because gcd(7, 12) = 1, the transposition T₇ cycles through every pitch class. From that one fact flows the organization of key signatures, the measurement of harmonic distance, the structure of common chord progressions, and the logic of modulation. It is the map of tonal music, and its entire content is the equation 7 × 12 ≡ 0 (mod 12) reached only after visiting every point along the way.

# Part VI: MODES

The major scale's step pattern [2, 2, 1, 2, 2, 2, 1] is a sequence of seven numbers that sum to 12. It wraps around the chromatic circle and lands back where it started. Played from a given root, it produces a specific set of seven pitch classes, and everything in Parts III through V treated that set as a single object.

But a sequence that wraps around a circle has no fixed beginning. The pattern [2, 2, 1, 2, 2, 2, 1] starts on its first element by convention. Start reading from the second element instead, wrapping around to pick up the first element at the end, and you get a different pattern: [2, 1, 2, 2, 2, 1, 2]. Apply this new pattern from the same root and you get a different set of pitch classes, a different sound, a different scale. This is a mode: a rotation of a step pattern. The seven diatonic modes are the seven rotations of the major scale pattern, and they have been in use, under various names and with varying prominence, for over two thousand years.

## VI.A. Modes as Rotations

Take the major scale step pattern and write it around a circle, seven numbers in a ring:

2, 2, 1, 2, 2, 2, 1

Now pick a starting position. Read clockwise, collecting seven numbers before returning to where you began. Each starting position yields a different ordering of the same seven step sizes.

Rotation 0 starts at position 1: [2, 2, 1, 2, 2, 2, 1]. This is the major scale itself, also called the Ionian mode.

Rotation 1 starts at position 2: [2, 1, 2, 2, 2, 1, 2]. This is the Dorian mode.

Rotation 2 starts at position 3: [1, 2, 2, 2, 1, 2, 2]. The Phrygian mode.

Rotation 3 starts at position 4: [2, 2, 2, 1, 2, 2, 1]. The Lydian mode.

Rotation 4 starts at position 5: [2, 2, 1, 2, 2, 1, 2]. The Mixolydian mode.

Rotation 5 starts at position 6: [2, 1, 2, 2, 1, 2, 2]. The Aeolian mode. This is the natural minor scale from Part III.

Rotation 6 starts at position 7: [1, 2, 2, 1, 2, 2, 2]. The Locrian mode.

Seven positions, seven modes. No new pitch classes are introduced. If you build all seven modes starting on the seven degrees of a single major scale, every mode uses the same set of pitch classes, just entered from a different door. The Dorian mode starting on PC 2 uses the same pitch classes as the Ionian mode starting on PC 0: both produce {0, 2, 4, 5, 7, 9, 11}. The modes are already inside every major scale, hiding in plain sight.

The names are Greek, inherited from medieval music theory, which itself inherited them (with some confusion and renaming) from ancient Greek theory.[^32] The names carry no mathematical content. What matters is the rotation number and the step pattern it produces.

The analogy to clock arithmetic is exact. A rotation of a circular sequence is the same operation as adding a constant to an index modulo the sequence length. Rotation k of a length-7 sequence S is the sequence S[(k + i) mod 7] for i = 0, 1, ..., 6. The seven diatonic modes are Z₇ acting on a length-7 circular sequence. This is a cyclic group of order 7, the same algebraic structure we saw in Z₁₂, just smaller.

One conceptual point deserves emphasis. The modes are not seven different constructions. They are one construction, the major scale step pattern, viewed from seven vantage points. A mode is a perspective on a pattern, not a new pattern. This is why experienced musicians sometimes describe modes as "the same notes, different home base." The pitch classes stay fixed. The hierarchy shifts.

## VI.B. The Seven Diatonic Modes

Building a mode requires two inputs: a root pitch class and a mode number. The mode number selects which rotation of the major step pattern to use, and the root determines where to begin applying it.

> **Algorithm: Build Mode**
>
> **Input:** A root pitch class r in Z₁₂, and a mode number m (1 through 7).
>
> **Output:** A set of 7 pitch classes forming the mode.
>
> **Step 1.** Let S = [2, 2, 1, 2, 2, 2, 1] be the major scale step pattern.
>
> **Step 2.** Rotate S by (m - 1) positions to get S'. That is, S'[i] = S[(i + m - 1) mod 7] for i = 0, ..., 6.
>
> **Step 3.** Set p₀ = r. For i = 1 through 6, compute pᵢ = (pᵢ₋₁ + S'[i - 1]) mod 12.
>
> **Step 4.** Return {p₀, p₁, p₂, p₃, p₄, p₅, p₆}.

The following table summarizes all seven modes. For clarity, each mode is built on root 0, so the resulting pitch classes can be compared directly.

| Mode | Name | Rotation | Step pattern | PCs on root 0 |
|:---:|:---|:---:|:---|:---|
| 1 | Ionian | 0 | [2, 2, 1, 2, 2, 2, 1] | {0, 2, 4, 5, 7, 9, 11} |
| 2 | Dorian | 1 | [2, 1, 2, 2, 2, 1, 2] | {0, 2, 3, 5, 7, 9, 10} |
| 3 | Phrygian | 2 | [1, 2, 2, 2, 1, 2, 2] | {0, 1, 3, 5, 7, 8, 10} |
| 4 | Lydian | 3 | [2, 2, 2, 1, 2, 2, 1] | {0, 2, 4, 6, 7, 9, 11} |
| 5 | Mixolydian | 4 | [2, 2, 1, 2, 2, 1, 2] | {0, 2, 4, 5, 7, 9, 10} |
| 6 | Aeolian | 5 | [2, 1, 2, 2, 1, 2, 2] | {0, 2, 3, 5, 7, 8, 10} |
| 7 | Locrian | 6 | [1, 2, 2, 1, 2, 2, 2] | {0, 1, 3, 5, 6, 8, 10} |

Several patterns are visible. All seven PC sets contain 0 and 7 (the root and the fifth), except Locrian, which contains 0 and 6 (a diminished fifth). This anomaly is one reason Locrian rarely functions as a tonal center in practice: the fifth above the root is diminished, robbing the mode of the stable P5 that anchors the other six.

Ionian and Lydian share six of their seven PCs. They differ only in the fourth degree: PC 5 in Ionian, PC 6 in Lydian. Ionian and Mixolydian also share six PCs, differing only in the seventh degree: PC 11 in Ionian, PC 10 in Mixolydian. These near-matches produce modes that sound closely related to the major scale, with a single altered note coloring the whole structure.

**Worked Example 40.** Build the Dorian mode (mode 2) on root 5. The step pattern is [2, 1, 2, 2, 2, 1, 2]. Starting from 5: 5, (5+2)=7, (7+1)=8, (8+2)=10, (10+2)=0, (0+2)=2, (2+1)=3. The PC set is {5, 7, 8, 10, 0, 2, 3}. In letter-name terms, this is F Dorian: F, G, A♭, B♭, C, D, E♭. Verify: this is the same set of pitch classes as the E♭ major scale (PC set {3, 5, 7, 8, 10, 0, 2}), entered from F instead of E♭.

**Worked Example 41.** Build the Lydian mode (mode 4) on root 7. Step pattern: [2, 2, 2, 1, 2, 2, 1]. From 7: 7, 9, 11, 1, 2, 4, 6. PC set: {7, 9, 11, 1, 2, 4, 6}. In traditional terms, G Lydian: G, A, B, C♯, D, E, F♯. The same pitch classes as D major ({2, 4, 6, 7, 9, 11, 1}), started from the fourth degree.

**Worked Example 42.** Build the Phrygian mode (mode 3) on root 4. Step pattern: [1, 2, 2, 2, 1, 2, 2]. From 4: 4, 5, 7, 9, 11, 0, 2. PC set: {4, 5, 7, 9, 11, 0, 2}. This is E Phrygian: E, F, G, A, B, C, D. The same pitch classes as C major, entered from the third degree. The characteristic sound of Phrygian comes from that opening semitone step, PC 4 to PC 5. This half-step above the root gives Phrygian its dark, Spanish-inflected quality.[^33]

There is a useful shortcut for determining which major scale a mode belongs to. Mode m on root r uses the same PC set as the Ionian mode (major scale) on root (r − c) mod 12, where c is the cumulative sum of the first (m − 1) steps of the major pattern. For Dorian (m = 2), c = 2. For Phrygian, c = 2 + 2 = 4. For Lydian, c = 2 + 2 + 1 = 5. For Mixolydian, c = 2 + 2 + 1 + 2 = 7. For Aeolian, c = 2 + 2 + 1 + 2 + 2 = 9. For Locrian, c = 2 + 2 + 1 + 2 + 2 + 2 = 11. So Dorian on root r shares its PC set with the major scale on root (r − 2) mod 12. Phrygian on r shares with major on (r − 4) mod 12. And so on. This is not a new fact. It follows directly from the definition of rotation.

## VI.C. Modal Brightness Ordering

Each mode built on root 0 differs from the Ionian (major) baseline in specific scale degrees. Those differences are what give each mode its characteristic color. Comparing the PC sets systematically reveals a natural ordering from "brightest" to "darkest."

The baseline is Ionian on root 0: {0, 2, 4, 5, 7, 9, 11}. Label the scale degrees 1 through 7, corresponding to PCs 0, 2, 4, 5, 7, 9, 11.

Lydian on root 0: {0, 2, 4, 6, 7, 9, 11}. Compared to Ionian, the only difference is the fourth degree: PC 6 instead of PC 5. The fourth is raised by one semitone. Musicians describe this as a "raised fourth" or "sharp four." Since raising a scale degree brightens the sound (pushing it further from the minor quality), Lydian is brighter than Ionian. It is the brightest of the seven diatonic modes.

Ionian on root 0: {0, 2, 4, 5, 7, 9, 11}. The major scale is the reference point.

Mixolydian on root 0: {0, 2, 4, 5, 7, 9, 10}. One degree lowered: the seventh drops from PC 11 to PC 10. A "flatted seventh." Darker than Ionian by one step.

Dorian on root 0: {0, 2, 3, 5, 7, 9, 10}. Two degrees lowered from Ionian: the third (PC 3 instead of 4) and the seventh (PC 10 instead of 11). The lowered third makes it minor. But the sixth degree remains at PC 9 (the same as in Ionian), giving Dorian a distinctly bright quality among the minor modes.

Aeolian on root 0: {0, 2, 3, 5, 7, 8, 10}. Three degrees lowered: the third (PC 3), sixth (PC 8 instead of 9), and seventh (PC 10). This is natural minor, darker than Dorian because the sixth has dropped.

Phrygian on root 0: {0, 1, 3, 5, 7, 8, 10}. Four degrees lowered: the second (PC 1 instead of 2), third (PC 3), sixth (PC 8), and seventh (PC 10). The lowered second is the hallmark of Phrygian and the source of its distinctive darkness.

Locrian on root 0: {0, 1, 3, 5, 6, 8, 10}. Five degrees lowered: the second, third, fifth (PC 6 instead of 7), sixth, and seventh. The diminished fifth robs Locrian of the stable P5 that every other mode possesses.

The brightness ordering, from brightest to darkest:

**Lydian > Ionian > Mixolydian > Dorian > Aeolian > Phrygian > Locrian**

Each step down the ladder lowers one additional scale degree by one semitone. Lydian has zero lowered degrees (relative to itself, or one raised degree relative to Ionian). Ionian is the baseline. Mixolydian lowers one. Dorian lowers two. Aeolian lowers three. Phrygian lowers four. Locrian lowers five.

The order in which degrees get lowered follows a specific sequence: 4th (raised in Lydian, so first to drop), then 7th, 3rd, 6th, 2nd, 5th. Written as PCs that change going down the ladder: 5→6 (Lydian to Ionian reversal), 11→10, 4→3, 9→8, 2→1, 7→6. This sequence, 4th, 7th, 3rd, 6th, 2nd, 5th, traces the circle of fifths applied to scale degrees. The brightness ordering is the circle of fifths in disguise.[^34]

This is not a coincidence. The circle of fifths orders pitch classes by harmonic proximity. Lowering a scale degree by one semitone corresponds to moving one step counterclockwise on the circle of fifths when measured among the scale degrees. The brightness spectrum of modes is a projection of the circle of fifths onto the seven-note diatonic framework.

For a musician, the practical value of the brightness ordering is immediate. Need a mode slightly darker than major? Mixolydian. Need minor but not too dark? Dorian. Need something exotic and tense? Phrygian. The ladder provides a continuum of shading between the extremes of Lydian brightness and Locrian instability.

## VI.D. Modes Beyond the Diatonic

The concept of modal rotation is not limited to the major scale. Any scale with a step pattern can be rotated, and each rotation produces a mode. Two non-diatonic parent scales are particularly important.

The harmonic minor scale has the step pattern [2, 1, 2, 2, 1, 3, 1]. Applied from root 0: {0, 2, 3, 5, 7, 8, 11}. The distinctive feature is that 3-semitone gap between the sixth and seventh degrees (PC 8 to PC 11), which gives harmonic minor its characteristic augmented second and its dramatic, often "Eastern" quality.

Rotating this pattern produces seven modes, each with its own character. The most frequently encountered is the fifth rotation, sometimes called Phrygian dominant: step pattern [1, 3, 1, 2, 1, 2, 2]. Built on root 0, this gives {0, 1, 4, 5, 7, 8, 10}. The combination of a lowered second (PC 1) with a major third (PC 4) produces a sound widely associated with flamenco, Middle Eastern music, and klezmer.[^35] The third mode of harmonic minor, sometimes called Ionian augmented, has pattern [2, 2, 1, 3, 1, 2, 1] and features an augmented fifth (PC 8 instead of 7 when built on root 0 from the appropriate rotation).

The melodic minor scale (ascending form) has the step pattern [2, 1, 2, 2, 2, 2, 1]. From root 0: {0, 2, 3, 5, 7, 9, 11}. Its modes include several that are staples of jazz harmony. The fourth rotation, [2, 2, 2, 1, 2, 1, 2], is the Lydian dominant scale: it combines Lydian's raised fourth with Mixolydian's lowered seventh. Built on root 0: {0, 2, 4, 6, 7, 9, 10}. This scale fits naturally over dominant seventh chords with a raised eleventh, a bread-and-butter sound in jazz improvisation.[^36]

The seventh rotation of melodic minor, [1, 2, 1, 2, 2, 2, 2], is the altered scale (also called the super-Locrian mode). Built on root 0: {0, 1, 3, 4, 6, 8, 10}. Every scale degree except the root and the flatted seventh is altered relative to the major scale. This maximally dark mode is used in jazz over altered dominant chords (dominant sevenths with flatted and sharped ninths, sharped elevenths, and flatted thirteenths). Its sound is dense and dissonant, the extreme end of modal darkness.

The principle at work is general. Any parent scale with n distinct step sizes arranged in a circular pattern of length n produces n modes by rotation. The diatonic scale has 7. Harmonic minor has 7. Melodic minor has 7. The pentatonic scale [2, 2, 3, 2, 3] has 5 modes. Even the whole-tone scale [2, 2, 2, 2, 2, 2] can be "rotated," though since all its steps are identical, every rotation yields the same pattern. A scale whose rotations are all identical has only one mode. A scale whose rotations are all distinct has as many modes as it has notes.

One final concept bridges modes and chords. Modal interchange is the practice of borrowing chords from a parallel mode. If a piece is in (0, Ionian) and uses the chord built on scale degree IV, that chord contains PCs {5, 9, 0}, a major triad on PC 5. Switching momentarily to (0, Aeolian), the chord on scale degree IV becomes {5, 8, 0}, a minor triad on PC 5, because Aeolian's sixth degree is PC 8 instead of 9. Importing this minor IV chord into an otherwise Ionian context is modal interchange. The technique is everywhere in popular music. A major-key song that drops in a "flat VII" chord (built on PC 10, borrowed from Mixolydian) or a "flat III" chord (built on PC 3, borrowed from Aeolian) is using modal interchange.[^37]

The full treatment of modal interchange requires the chord vocabulary that Part VII will establish. For now, the key idea is that modes are not sealed compartments. Composers and songwriters move between parallel modes freely, borrowing pitch classes and the chords they generate, creating color shifts that a single mode could not produce on its own.

---

# Part VII: CHORDS

A melody is a sequence of pitch classes unfolding in time. A chord is a set of pitch classes sounding at once. Where melody is horizontal, chords are vertical. The two together, melody moving over a foundation of chords, form the harmonic language of nearly all Western music from the Renaissance forward.

In the integer system, a chord is simply a subset of Z₁₂. A three-note chord is a 3-element subset. A four-note chord is a 4-element subset. The intervals between the elements determine the chord's quality: major, minor, diminished, augmented, dominant, and so on. These labels, like interval names, are aliases for specific numerical configurations. The numbers come first. The names follow.

## VII.A. Chords as Pitch-Class Sets

A chord type is defined by a set of intervals measured from a root. The root is the pitch class that gives the chord its name, and the intervals are fixed distances above the root.

Consider the major triad. Its interval template is {0, 4, 7}: the root, a note 4 semitones above it (a major third), and a note 7 semitones above it (a perfect fifth). To build a major triad on any root r, apply the template: {r, (r + 4) mod 12, (r + 7) mod 12}. The template is abstract. A specific chord is the template anchored to a root.

This separation between template and instance is the same distinction that Part III drew between a step pattern and a specific scale. A scale type is a step pattern. A specific scale is a step pattern applied from a root. A chord type is an interval template. A specific chord is an interval template applied from a root. Both operations are transposition in Z₁₂: adding a constant to every element of a set.

The root's role deserves a moment of attention. In the pitch-class set {0, 4, 7}, no element is algebraically privileged. The set is the set. But musically, one member is designated the root, and that designation determines how the chord is named, how it functions in a key, and how it resolves. The chord {0, 4, 7} with root 0 is "C major." The same three pitch classes with root 4 would be something different entirely (an inversion of C major, not E something). The root is metadata attached to the set, not a property derivable from the set alone.[^38]

In practice, the root is usually the lowest-sounding note, or the note from which the chord was built by stacking thirds, or the note that a listener perceives as the chord's foundation. These criteria almost always agree, and in the standard cases covered in this Part, they do agree. Ambiguous cases exist, but they are rare enough to handle individually when they arise.

## VII.B. Triads: The Four Types

A triad is a three-note chord built by stacking two intervals of a third (3 or 4 semitones) above a root. Since each third can be major (4 semitones) or minor (3 semitones), there are four possible combinations.

> **Algorithm: Build Triad**
>
> **Input:** A root pitch class r in Z₁₂, and a triad type (major, minor, diminished, or augmented).
>
> **Output:** A set of 3 pitch classes.
>
> **Step 1.** Select the interval template based on triad type:
>
> - Major: {0, 4, 7} (M3 + m3)
> - Minor: {0, 3, 7} (m3 + M3)
> - Diminished: {0, 3, 6} (m3 + m3)
> - Augmented: {0, 4, 8} (M3 + M3)
>
> **Step 2.** Add r to each element of the template, mod 12: {r, (r + a) mod 12, (r + b) mod 12}, where {0, a, b} is the selected template.

The four types in detail:

| Triad type | Template | Interval structure | Third 1 | Third 2 | Total span |
|:---|:---|:---|:---:|:---:|:---:|
| Major | {0, 4, 7} | root, M3, P5 | 4 (M3) | 3 (m3) | 7 (P5) |
| Minor | {0, 3, 7} | root, m3, P5 | 3 (m3) | 4 (M3) | 7 (P5) |
| Diminished | {0, 3, 6} | root, m3, d5 | 3 (m3) | 3 (m3) | 6 (tritone) |
| Augmented | {0, 4, 8} | root, M3, A5 | 4 (M3) | 4 (M3) | 8 (m6) |

Notice the symmetry. Major and minor are mirror images: M3 + m3 versus m3 + M3. Both span a perfect fifth (7 semitones) from root to top note. They differ only in the internal split of that fifth. The major triad divides the P5 into 4 + 3. The minor triad divides it into 3 + 4. This inversional relationship between major and minor triads is a preview of a deeper symmetry that Part XII will explore.

Diminished and augmented are the symmetric cases: two equal thirds stacked. The diminished triad uses two minor thirds (3 + 3 = 6), spanning a tritone. The augmented triad uses two major thirds (4 + 4 = 8), spanning a minor sixth. Both have a distinctive, unstable sound. The diminished triad's tritone creates tension that seeks resolution. The augmented triad's equal division of the octave into three parts (since 4 + 4 + 4 = 12) gives it a floating, directionless quality.[^39]

**Worked Example 43.** Build a major triad on root 7. Template {0, 4, 7}, shifted by 7: {7, (7+4) mod 12, (7+7) mod 12} = {7, 11, 2}. In letter names: G, B, D. This is G major.

**Worked Example 44.** Build a minor triad on root 2. Template {0, 3, 7}, shifted by 2: {2, (2+3) mod 12, (2+7) mod 12} = {2, 5, 9}. In letter names: D, F, A. This is D minor.

**Worked Example 45.** Build a diminished triad on root 11. Template {0, 3, 6}, shifted by 11: {11, (11+3) mod 12, (11+6) mod 12} = {11, 2, 5}. In letter names: B, D, F. This is B diminished. The interval from 11 to 5 is (5 − 11) mod 12 = 6, a tritone. No perfect fifth anywhere in this chord.

**Worked Example 46.** Build an augmented triad on root 0. Template {0, 4, 8}: {0, 4, 8}. In letter names: C, E, G♯. Now build augmented on root 4: {4, 8, 0}. Same three pitch classes, different root. And on root 8: {8, 0, 4}. Again the same three PCs. The augmented triad on roots 0, 4, and 8 all produce the same set {0, 4, 8}. Since the augmented triad divides the octave into three equal parts (4 + 4 + 4 = 12), there are only four distinct augmented triads: {0, 4, 8}, {1, 5, 9}, {2, 6, 10}, and {3, 7, 11}. Each serves triple duty, named after whichever of its three members is designated root.

The interval vector for both major and minor triads is [0, 0, 1, 1, 1, 0]. This means each triad contains exactly one interval class of size 3 (a minor third), one of size 4 (a major third), and one of size 5 (a perfect fourth/fifth). No semitones, no whole tones, no tritones. The diminished triad's interval vector is [0, 0, 2, 0, 0, 1]: two minor thirds and one tritone. The augmented triad's interval vector is [0, 0, 0, 2, 0, 0] (if we restrict to interval classes 1 through 5) or more precisely [0, 0, 0, 3, 0, 0] counting all pairs. These vectors quantify what the ear reports: major and minor triads are consonant (no semitones or tritones), diminished triads are tense (a tritone), and augmented triads are strange (nothing but major thirds, no fifth to ground them).

## VII.C. Seventh Chords

Stack one more third on top of a triad and the result is a seventh chord: four pitch classes, the highest of which is a seventh interval (10 or 11 semitones) above the root. The added note thickens the sound and, depending on the combination, adds either warmth or tension.

Five types of seventh chord appear regularly in tonal and popular music.

**Major seventh (maj7).** Template: {0, 4, 7, 11}. A major triad plus a major seventh. The interval from root to top is 11 semitones (M7). The sound is lush and stable, the "jazz ballad" chord. Built on root 0: {0, 4, 7, 11}. In letter terms: C, E, G, B.

**Dominant seventh (dom7, or simply "7").** Template: {0, 4, 7, 10}. A major triad plus a minor seventh. The interval from root to top is 10 semitones (m7). This chord contains a tritone between its third and seventh: (10 − 4) mod 12 = 6. That internal tritone is the engine of tension and resolution in tonal harmony. Built on root 0: {0, 4, 7, 10}. In letter terms: C, E, G, B♭.

**Minor seventh (min7, or m7).** Template: {0, 3, 7, 10}. A minor triad plus a minor seventh. Warm, mellow, neither tense nor fully resolved. Built on root 0: {0, 3, 7, 10}. In letter terms: C, E♭, G, B♭.

**Half-diminished seventh (ø7).** Template: {0, 3, 6, 10}. A diminished triad plus a minor seventh. The diminished fifth and the minor seventh together give it a dark, yearning sound. Built on root 0: {0, 3, 6, 10}. In letter terms: C, E♭, G♭, B♭.

**Fully diminished seventh (°7).** Template: {0, 3, 6, 9}. A diminished triad plus a diminished seventh (9 semitones). Every adjacent pair of notes is separated by exactly 3 semitones: 0 to 3, 3 to 6, 6 to 9, 9 back to 0. Four notes dividing the octave into four equal parts. This perfect symmetry has a striking consequence: there are only three distinct fully diminished seventh chords. The chord {0, 3, 6, 9} is the same set as the chord built on root 3 ({3, 6, 9, 0}), root 6 ({6, 9, 0, 3}), or root 9 ({9, 0, 3, 6}). Similarly, {1, 4, 7, 10} and {2, 5, 8, 11} are the other two. Twelve possible roots, three distinct chords. Each fully diminished seventh is a square inscribed in the chromatic circle.[^40]

| Seventh chord type | Template | Triad base | Added interval | Internal tritone? |
|:---|:---|:---|:---|:---:|
| Major 7th (maj7) | {0, 4, 7, 11} | Major | M7 (11) | No |
| Dominant 7th (7) | {0, 4, 7, 10} | Major | m7 (10) | Yes: between 4 and 10 |
| Minor 7th (m7) | {0, 3, 7, 10} | Minor | m7 (10) | No |
| Half-diminished (ø7) | {0, 3, 6, 10} | Diminished | m7 (10) | Yes: between 0 and 6 |
| Fully diminished (°7) | {0, 3, 6, 9} | Diminished | d7 (9) | Yes: between 0 and 6, and between 3 and 9 |

The "Internal tritone?" column matters because tritones create harmonic tension. The dominant seventh chord has exactly one tritone (between its third and seventh), which is why it is the primary tension-generating chord in tonal music. The fully diminished seventh has two tritones, making it even more unstable, a chord that resolves urgently in almost any direction.

**Worked Example 47.** Build a dominant seventh on root 7. Template {0, 4, 7, 10}, shifted by 7: {7, 11, 2, 5}. In letter terms: G, B, D, F. This is G7, the V7 chord in the key of 0 (C major). The tritone sits between PCs 11 and 5 (B and F): (5 − 11) mod 12 = 6. This tritone is the reason G7 resolves so powerfully to C major. The B wants to rise to C (11 → 0, one semitone up), and the F wants to fall to E (5 → 4, one semitone down). Both tritone members resolve by semitone motion to members of the tonic triad. This mechanism will be central to Part VIII.

**Worked Example 48.** Build a fully diminished seventh on root 2. Template {0, 3, 6, 9}, shifted by 2: {2, 5, 8, 11}. Check: is this the same as the diminished seventh on root 5? Shift template by 5: {5, 8, 11, 2}. Same set. On root 8: {8, 11, 2, 5}. Same set again. On root 11: {11, 2, 5, 8}. Same set. Four roots, one chord. The symmetry of equal division.

## VII.D. Inversions and Voicings

A chord's pitch-class set does not specify which note is lowest. The set {0, 4, 7} might be played as C in the bass with E and G above it, or as E in the bass with G and C above, or as G in the bass with C and E above. These arrangements are called inversions.

Root position places the root in the bass. First inversion places the third in the bass. Second inversion places the fifth in the bass. For seventh chords, there is also third inversion, which places the seventh in the bass.

| Position | Bass note | Traditional figured bass |
|:---|:---|:---|
| Root position | Root | 5/3 (or just the chord name) |
| First inversion | Third | 6/3 (or just "6") |
| Second inversion | Fifth | 6/4 |
| Third inversion (7th chords) | Seventh | 4/2 |

The pitch-class set is the same in every inversion. {0, 4, 7} stays {0, 4, 7} regardless of which element sits in the lowest octave. In the PC-set framework, inversions are not different chords. They are different voicings of the same chord. The harmony is identical. What changes is the bass line, and bass lines matter for voice leading (Part VIII) and for the sense of stability or motion that a passage conveys.

Root position is the most stable voicing. The root in the bass reinforces the chord's identity, aligning with the overtone series of the bass note. First inversion is lighter, more mobile. It smooths out bass lines by allowing stepwise motion between chords. Second inversion is the least stable of the three for triads. In common-practice harmony, the 6/4 position is treated with care, often reserved for specific contexts: cadential approach chords, passing motion, or pedal points.[^41]

Slash chord notation expresses inversions concisely. "C/E" means a C major chord with E in the bass, which is {0, 4, 7} with PC 4 in the lowest voice. First inversion. "C/G" means {0, 4, 7} with PC 7 in the bass. Second inversion. The notation generalizes beyond inversions: "C/B♭" would put PC 10 in the bass under a C major triad, which is not a standard inversion of C major at all but a voicing of C7 (dominant seventh on C) with the seventh in the bass (third inversion).

For the purposes of harmonic analysis, which is the main concern of this book, inversions are a secondary matter. Two chords with the same PC set and the same root are the same chord, harmonically. The difference between root position and first inversion is a difference in texture and voice movement, not in harmonic function. This is the advantage of the pitch-class approach: it separates the essential (which PCs are sounding) from the ornamental (which octave each PC occupies) and lets each be analyzed independently.

**Worked Example 49.** The chord {5, 9, 0} is a major triad with root 5 (F major: F, A, C). In root position, the bass note is 5 (F). First inversion: bass note 9 (A), notated F/A. Second inversion: bass note 0 (C), notated F/C. All three voicings function as the IV chord in the key of (0, major).

## VII.E. Extended Chords: Ninths, Elevenths, Thirteenths

Seventh chords stack three thirds above a root. The process can continue. Each additional third adds another note, extending the chord further up the scale.

The naming convention uses scale-degree numbers that extend past the octave. The ninth is the second scale degree displaced up an octave: (r + 2) mod 12 in pitch-class terms, since the compound interval of a ninth (14 semitones) reduces to 2 mod 12. The eleventh is the fourth degree up an octave: (r + 5) mod 12. The thirteenth is the sixth degree up an octave: (r + 9) mod 12.

An extended chord includes the seventh and all extensions up to the named degree:

A **ninth chord** is a seventh chord plus the ninth: 5 pitch classes. A dominant ninth on root 0: {0, 4, 7, 10, 2}.

An **eleventh chord** adds the eleventh: 6 pitch classes. A dominant eleventh on root 0: {0, 4, 7, 10, 2, 5}.

A **thirteenth chord** adds the thirteenth: 7 pitch classes. A dominant thirteenth on root 0: {0, 4, 7, 10, 2, 5, 9}.

**Worked Example 50.** Build a dominant thirteenth chord on root 0 and compare it with the C major scale. The chord: {0, 4, 7, 10, 2, 5, 9}. Rewrite in ascending order: {0, 2, 4, 5, 7, 9, 10}. The major scale on root 0: {0, 2, 4, 5, 7, 9, 11}. These two sets differ in exactly one element: the chord has PC 10 where the scale has PC 11. A full thirteenth chord contains all seven scale degrees, with the seventh degree flatted (minor seventh instead of major seventh). The dominant thirteenth is, in effect, the entire major scale reharmonized with a dominant function. Seven notes sounding simultaneously (or arpeggiated), the complete harmonic palette of the key, with only the quality of the seventh distinguishing chord from scale.

In practice, not all notes of an extended chord are sounded. A full thirteenth chord played with all seven notes can sound muddy, and performers routinely omit tones to clarify the harmony. The fifth is the most common omission, since it adds little to the chord's color. In dominant chords, the eleventh is often raised by a semitone (to PC 6 instead of 5 when the root is 0) to avoid a minor ninth clash between the third (PC 4) and the natural eleventh (PC 5). This raised eleventh is notated as ♯11 and produces the Lydian dominant sound described in Part VI.

The extensions (9th, 11th, 13th) can be altered: raised or lowered by a semitone from their default position. These alterations produce a wide vocabulary of chord colors. A dominant 7♯9 on root 0 replaces the natural ninth (PC 2) with a raised ninth (PC 3): {0, 4, 7, 10, 3}. This chord, containing both a major third (PC 4) and a minor third (PC 3), is the famous "Hendrix chord," a staple of blues-rock and funk.[^42] A dominant 7♭9 lowers the ninth: {0, 4, 7, 10, 1}. Each alteration tilts the chord brighter or darker, and the possibilities multiply with each extension.

The arithmetic is simple. To build any extended or altered chord: start with the template for the base seventh chord, then add (r + d) mod 12 for each extension d, where d is 2 (ninth), 5 (eleventh), or 9 (thirteenth), adjusted by +1 or -1 for any sharp or flat alteration.

## VII.F. Suspended and Added-Tone Chords

Not every chord is built by stacking thirds. Some replace the third with a neighboring scale degree, and others add a note to a triad without including the seventh.

**Sus2.** Template: {0, 2, 7}. The third is replaced by a second: the interval from root to second member is 2 semitones (M2) instead of 3 or 4. Built on root 0: {0, 2, 7}. In letter terms: C, D, G. The chord has an open, ambiguous quality, neither major nor minor, because the note that determines major/minor quality (the third) is absent.

**Sus4.** Template: {0, 5, 7}. The third is replaced by a fourth: 5 semitones. Built on root 0: {0, 5, 7}. In letter terms: C, F, G. Like sus2, this chord avoids the major/minor distinction. The fourth creates a sense of suspension, a note hanging above where the third "should" be, generating expectation that it will fall back down. The name "sus" is short for "suspended."[^43]

**Add9.** Template: {0, 4, 7, 2} (for major add9). This is a major triad plus the ninth, without a seventh in between. The omission of the seventh distinguishes add9 from a ninth chord. Built on root 0: {0, 2, 4, 7}. In letter terms: C, D, E, G. The add9 has a bright, shimmering quality popular in pop and folk music.

**Add11.** Template: {0, 4, 5, 7}. A major triad plus the eleventh. Less common than add9, because the eleventh (PC 5) sits one semitone above the third (PC 4), creating a semitone dissonance. Some styles embrace that tension; others avoid it.

**Power chord.** Template: {0, 7}. Just the root and the fifth. Two pitch classes, no third. This is the stripped-down chord of rock and metal, played on electric guitar with heavy distortion. The absence of the third means the chord is neither major nor minor. It is pure root and fifth, bare harmonic scaffolding. In the pitch-class framework, a power chord is a 2-element subset of Z₁₂, the smallest structure that deserves the name "chord" (a single note is just a pitch class, not a chord).

The difference between "sus" and "add" is structural. A sus chord replaces the third. An add chord keeps the third and supplements it. Csus4 = {0, 5, 7} has no third. Cadd11 = {0, 4, 5, 7} has both the third and the fourth. The former is a substitution. The latter is an addition.

**Worked Example 51.** Build sus4 on root 7. Template {0, 5, 7}, shifted by 7: {7, 0, 2}. In letter terms: G, C, D. This is Gsus4. The C (PC 0) sits where B (PC 11) would be in a G major triad. The fourth (C) is "suspended" above the third (B), creating tension. When the C resolves down to B, the chord becomes G major: {7, 11, 2}. This sus4-to-major resolution is one of the most common harmonic gestures in popular music.

## VII.G. Building Chords on Scale Degrees

Every chord type discussed so far has been built using a fixed template, a set of intervals from the root chosen by the musician. But when harmony operates within a key, a different construction takes priority: building chords using only the pitch classes available in the scale. The scale itself determines which chord types arise on each degree, and the results are not arbitrary. They follow from the arithmetic of the step pattern.

> **Algorithm: Diatonic Triads**
>
> **Input:** A scale S = {s₀, s₁, s₂, s₃, s₄, s₅, s₆} (7 PCs in scale order) and a degree d (1 through 7).
>
> **Output:** A triad built on degree d using only PCs from S.
>
> **Step 1.** Let the root be s_{d-1} (the PC at position d in the scale, zero-indexed as d - 1).
>
> **Step 2.** The third is s_{(d+1) mod 7} (skip one scale member).
>
> **Step 3.** The fifth is s_{(d+3) mod 7} (skip two more, equivalently skip one from the third).
>
> **Step 4.** Return {root, third, fifth}. Determine the triad type from the intervals between them.

Apply this algorithm to the major scale on root 0: S = {0, 2, 4, 5, 7, 9, 11}.

**Degree 1 (root PC 0).** Third: PC 4. Fifth: PC 7. Chord: {0, 4, 7}. Intervals from root: 4 and 7. Template {0, 4, 7} = major. Roman numeral: **I**.

**Degree 2 (root PC 2).** Third: PC 5. Fifth: PC 9. Chord: {2, 5, 9}. Intervals from root: (5-2)=3, (9-2)=7. Template {0, 3, 7} = minor. Roman numeral: **ii**.

**Degree 3 (root PC 4).** Third: PC 7. Fifth: PC 11. Chord: {4, 7, 11}. Intervals: (7-4)=3, (11-4)=7. Template {0, 3, 7} = minor. Roman numeral: **iii**.

**Degree 4 (root PC 5).** Third: PC 9. Fifth: PC 0. Chord: {5, 9, 0}. Intervals: (9-5)=4, (0-5) mod 12=7. Template {0, 4, 7} = major. Roman numeral: **IV**.

**Degree 5 (root PC 7).** Third: PC 11. Fifth: PC 2. Chord: {7, 11, 2}. Intervals: (11-7)=4, (2-7) mod 12=7. Template {0, 4, 7} = major. Roman numeral: **V**.

**Degree 6 (root PC 9).** Third: PC 0. Fifth: PC 4. Chord: {9, 0, 4}. Intervals: (0-9) mod 12=3, (4-9) mod 12=7. Template {0, 3, 7} = minor. Roman numeral: **vi**.

**Degree 7 (root PC 11).** Third: PC 2. Fifth: PC 5. Chord: {11, 2, 5}. Intervals: (2-11) mod 12=3, (5-11) mod 12=6. Template {0, 3, 6} = diminished. Roman numeral: **vii°**.

The complete pattern:

| Degree | Root PC | Triad PCs | Type | Roman numeral |
|:---:|:---:|:---|:---|:---:|
| 1 | 0 | {0, 4, 7} | Major | I |
| 2 | 2 | {2, 5, 9} | Minor | ii |
| 3 | 4 | {4, 7, 11} | Minor | iii |
| 4 | 5 | {5, 9, 0} | Major | IV |
| 5 | 7 | {7, 11, 2} | Major | V |
| 6 | 9 | {9, 0, 4} | Minor | vi |
| 7 | 11 | {11, 2, 5} | Diminished | vii° |

The pattern **I, ii, iii, IV, V, vi, vii°** is not a convention chosen by committee. It is a theorem, derived from the major scale's step pattern by the algorithm above. Major triads appear on degrees 1, 4, and 5. Minor triads appear on degrees 2, 3, and 6. A diminished triad appears on degree 7. This holds for every major key, because every major key has the same step pattern. Only the pitch classes change. The chord qualities are invariant.

The Roman numeral notation encodes triad quality in its case: uppercase for major, lowercase for minor, with ° for diminished and + for augmented. This notation is standard across music theory and will be used throughout the remainder of the book.

**Worked Example 52.** Verify the pattern for the major scale on root 5 (F major). S = {5, 7, 9, 10, 0, 2, 4}.

Degree 1 (PC 5): third = PC 9, fifth = PC 0. Chord {5, 9, 0}. Intervals: 4, 7. Major. I.
Degree 2 (PC 7): third = PC 10, fifth = PC 2. Chord {7, 10, 2}. Intervals: 3, 7. Minor. ii.
Degree 3 (PC 9): third = PC 0, fifth = PC 4. Chord {9, 0, 4}. Intervals: 3, 7. Minor. iii.
Degree 4 (PC 10): third = PC 2, fifth = PC 5. Chord {10, 2, 5}. Intervals: 4, 7. Major. IV.
Degree 5 (PC 0): third = PC 4, fifth = PC 7. Chord {0, 4, 7}. Intervals: 4, 7. Major. V.
Degree 6 (PC 2): third = PC 5, fifth = PC 9. Chord {2, 5, 9}. Intervals: 3, 7. Minor. vi.
Degree 7 (PC 4): third = PC 7, fifth = PC 10. Chord {4, 7, 10}. Intervals: 3, 6. Diminished. vii°.

The pattern is identical: I, ii, iii, IV, V, vi, vii°. The algorithm produces the same chord-quality sequence regardless of root. This is the power of building on a step pattern rather than on letter names. The structure is portable.

Now extend the same method to seventh chords. Stack one more third from the scale on top of each triad: take every other scale tone, four notes deep instead of three.

**Degree 1 (PC 0).** Triad {0, 4, 7}, add seventh: PC 11. Chord: {0, 4, 7, 11}. The seventh interval: (11-0)=11 (M7). Template {0, 4, 7, 11} = major seventh. **Imaj7**.

**Degree 2 (PC 2).** Triad {2, 5, 9}, add seventh: PC 0. Chord: {2, 5, 9, 0}. Seventh interval: (0-2) mod 12=10 (m7). Template {0, 3, 7, 10} = minor seventh. **ii7**.

**Degree 3 (PC 4).** Triad {4, 7, 11}, add seventh: PC 2. Chord: {4, 7, 11, 2}. Seventh: (2-4) mod 12=10 (m7). Minor seventh. **iii7**.

**Degree 4 (PC 5).** Triad {5, 9, 0}, add seventh: PC 4. Chord: {5, 9, 0, 4}. Seventh: (4-5) mod 12=11 (M7). Major seventh. **IVmaj7**.

**Degree 5 (PC 7).** Triad {7, 11, 2}, add seventh: PC 5. Chord: {7, 11, 2, 5}. Seventh: (5-7) mod 12=10 (m7). But the triad is major, and the seventh is minor. Template {0, 4, 7, 10} = dominant seventh. **V7**.

**Degree 6 (PC 9).** Triad {9, 0, 4}, add seventh: PC 7. Chord: {9, 0, 4, 7}. Seventh: (7-9) mod 12=10 (m7). Minor seventh. **vi7**.

**Degree 7 (PC 11).** Triad {11, 2, 5}, add seventh: PC 9. Chord: {11, 2, 5, 9}. Seventh: (9-11) mod 12=10 (m7). Triad is diminished, seventh is minor. Template {0, 3, 6, 10} = half-diminished. **viiø7**.

The complete diatonic seventh-chord pattern:

| Degree | Root PC | Seventh chord PCs | Type | Roman numeral |
|:---:|:---:|:---|:---|:---:|
| 1 | 0 | {0, 4, 7, 11} | Major 7th | Imaj7 |
| 2 | 2 | {2, 5, 9, 0} | Minor 7th | ii7 |
| 3 | 4 | {4, 7, 11, 2} | Minor 7th | iii7 |
| 4 | 5 | {5, 9, 0, 4} | Major 7th | IVmaj7 |
| 5 | 7 | {7, 11, 2, 5} | Dominant 7th | V7 |
| 6 | 9 | {9, 0, 4, 7} | Minor 7th | vi7 |
| 7 | 11 | {11, 2, 5, 9} | Half-diminished | viiø7 |

The pattern: **Imaj7, ii7, iii7, IVmaj7, V7, vi7, viiø7**.

The most important observation in this table is the uniqueness of V7. Only one degree of the major scale produces a dominant seventh chord. Degree 5. No other. The dominant seventh template {0, 4, 7, 10} arises naturally on the fifth degree and nowhere else. This is why the V7 chord has its special name and its special role. It is the only diatonic chord that contains a tritone between its third and seventh (PCs 11 and 5 in the key of 0), and that tritone resolves by semitone motion to the root and third of the tonic chord: 11→0 and 5→4. The resolution V7→I is not a stylistic preference. It is a consequence of the step pattern arithmetic. The major scale generates exactly one chord with this pull toward the tonic, and it sits on degree 5.[^44]

**Worked Example 53.** In the key of (7, major), what is the V7 chord? The fifth degree of the G major scale (S = {7, 9, 11, 0, 2, 4, 6}) is PC 2 (D). The diatonic seventh chord on degree 5 is {2, 6, 9, 0}. Check: intervals from root 2 are (6-2)=4 (M3), (9-2)=7 (P5), (0-2) mod 12=10 (m7). Template {0, 4, 7, 10} = dominant seventh. This is D7. The tritone is between PCs 6 and 0 (F♯ and C): (0-6) mod 12=6. F♯ resolves up to G (6→7), C resolves down to B (0→11). Both move by one semitone into the tonic triad {7, 11, 2}. The V7→I resolution in G major mirrors the one in C major, transposed by 7 semitones.

**Worked Example 54.** Build the diatonic seventh chord on degree 4 of the major scale on root 9 (A major). S = {9, 11, 1, 2, 4, 6, 8}. Degree 4 is PC 2 (D). Stack thirds from the scale: root 2, third at PC 6, fifth at PC 9, seventh at PC 1. Chord: {2, 6, 9, 1}. Intervals from root: (6-2)=4 (M3), (9-2)=7 (P5), (1-2) mod 12=11 (M7). Template {0, 4, 7, 11} = major seventh. IVmaj7. In letter terms, this is Dmaj7. The algorithm produces the same chord quality (major seventh on degree 4) regardless of the key, because the step pattern is the same.

The diatonic chord patterns for minor scales follow the same algorithm. Apply the triad-building procedure to the natural minor scale on root 0, S = {0, 2, 3, 5, 7, 8, 10}, and the pattern that emerges is: i, ii°, III, iv, v, VI, VII. Minor triads on degrees 1 and 4, a diminished triad on degree 2, major triads on degrees 3, 6, and 7, and a minor triad on degree 5. When harmonic minor is used instead (with its raised seventh degree, PC 11 replacing PC 10), the chord on degree 5 becomes major, giving the minor key its own V chord with dominant function. This is why harmonic minor exists: to provide a dominant-to-tonic resolution in minor keys.

The ability to derive chord qualities from a scale pattern, rather than memorizing them, is perhaps the single most practical payoff of the integer approach. A musician who has internalized the algorithm can sit down in any key, compute the diatonic chords, and know which are major, which are minor, and which is diminished, without consulting a chart. The chart is a consequence. The algorithm is the source.

# Part VIII: HARMONIC FUNCTION AND PROGRESSIONS

Every chord in a key has a job. Not a fixed job, exactly, but a gravitational tendency, a role it falls into because of which pitch classes it shares with the tonic and which it does not. The previous parts built chords from intervals and scales from step patterns. This part asks a different question: given a key and its seven diatonic chords, how do those chords relate to each other? Why do certain chord sequences sound purposeful while others meander? The answer lies in three functional categories that have organized tonal harmony for centuries.

## VIII.A. Tonic, Subdominant, Dominant

The seven diatonic triads of a major key divide into three functional groups. The grouping is not arbitrary. It falls out of shared pitch-class content.

In any major key, the tonic triad (I) is the home chord, the point of rest. In the key of 0, I = {0, 4, 7}. The vi chord, {9, 0, 4}, shares two pitch classes with I: PCs 0 and 4. Because vi overlaps so heavily with I, it can substitute for the tonic without disrupting the sense of stability. These two chords form the **tonic function (T)**: I and vi. Both contain the tonic pitch class itself (PC 0) and the third of the scale (PC 4). They sound like home, or close enough to home that the ear accepts them as resting places.

The IV chord in the key of 0 is {5, 9, 0}. The ii chord is {2, 5, 9}. They share PCs 5 and 9. Neither chord contains the leading tone (PC 11), and both contain PC 5, the fourth scale degree, which carries a tendency to move rather than rest. These two chords form the **subdominant function (S)**: IV and ii. They represent departure, the sensation of having left home. The music has gone somewhere, and the listener feels the pull to continue rather than stop.

The V chord is {7, 11, 2}. The vii° chord is {11, 2, 5}. They share PCs 11 and 2. Both contain PC 11, the leading tone, the pitch class that sits one semitone below the tonic and pulls toward it with an almost physical insistence. These two chords form the **dominant function (D)**: V and vii°. They represent tension, the musical equivalent of a question that demands an answer. Dominant-function chords create the expectation of resolution. They point toward the tonic.

This leaves the iii chord, {4, 7, 11}. It shares PCs 4 and 7 with I (suggesting tonic function) but also contains PC 11 (suggesting dominant function). In practice, iii is a chameleon. It can serve as a weak tonic substitute or as a dominant substitute, depending on context. Most functional analyses treat iii as tonic-leaning, but it is the least committed member of any group.

The fundamental motion of tonal music follows one pattern: **T, then S, then D, then T again**. Home, departure, tension, resolution. A vast amount of Western music from the Baroque era through contemporary pop conforms to this cycle. Sometimes the cycle is compressed (D to T, skipping S). Sometimes S precedes D without an explicit T at the start. The cycle can be entered at any point and repeated indefinitely. But the ordering T to S to D to T is the gravitational default, the path that sounds most natural and complete.

Why does the T to S to D to T cycle feel so natural? Each transition increases harmonic tension by one step, and the final step releases all of it. Moving from I to IV introduces new pitch classes (PC 5 replaces PC 7 in the bass), shifting the tonal center away from home. Moving from IV to V replaces the subdominant's PCs with the dominant's, and the arrival of the leading tone (PC 11) ratchets the tension higher. The leading tone then resolves up by one semitone to the tonic, and the cycle closes.

The three-function model is a simplification. Real music constantly bends, extends, and subverts the pattern. But the simplification captures something genuine about how chord progressions create directed motion. A chord is not just a collection of simultaneous pitches. Within a key, it is a signpost that tells the listener where the music has been and where it is going.

## VIII.B. Diatonic Chord Progressions

A chord progression is a sequence of chords unfolding in time. Described in Roman numerals, a progression is key-independent: I-IV-V-I means the same thing in every major key. The Roman numerals specify function and scale-degree relationships. The actual pitch classes depend on the key.

Several progressions appear so frequently across genres and centuries that they deserve explicit attention.

**I-IV-V-I** is the simplest complete functional cycle. Tonic to subdominant to dominant to tonic. In the key of 0: {0, 4, 7} to {5, 9, 0} to {7, 11, 2} to {0, 4, 7}. Three chords, one full orbit. Folk music, hymns, blues, punk rock, and children's songs all rely on this backbone. It is the minimum viable progression.

**I-vi-IV-V** cycles through T, T, S, D. The initial tonic is reinforced by its functional partner vi before the music departs to IV and builds tension through V. When the sequence loops, V resolves back to I and the cycle restarts. This progression dominated American popular music in the 1950s, appearing in "Stand by Me," "Earth Angel," and dozens of doo-wop standards. It is sometimes called the "50s progression" or the "ice cream changes."

**I-V-vi-IV** rearranges those same four chords into a different emotional arc. The tonic moves directly to dominant (skipping subdominant), then retreats to vi (a tonic substitute, but minor, so it sounds bittersweet), and continues to IV (subdominant). The progression avoids a strong authentic cadence (V to I) because vi intercepts the resolution. This gives the sequence a quality of yearning, of never quite arriving. It is pervasive in pop music from the 2000s onward and was the subject of a well-known comedy sketch cataloging its ubiquity.[^45]

**vi-IV-I-V** is the same four chords starting from a different point in the cycle. Beginning on vi (minor) gives the progression a darker opening, even though the harmonic content is identical. The perception changes because the first chord sets the listener's expectations. A minor opening primes the ear for sadness or intensity, and the subsequent major chords feel like contrast rather than baseline.

**Worked Example 55.** Realize I-IV-V-I in the key of (7, major). The major scale from root 7, applying the step pattern [2, 2, 1, 2, 2, 2, 1]: 7, 9, 11, 0, 2, 4, 6. Scale degrees: 1st = 7, 2nd = 9, 3rd = 11, 4th = 0, 5th = 2, 6th = 4, 7th = 6. Diatonic triads built by stacking alternating scale degrees: I = {7, 11, 2}, IV = {0, 4, 7}, V = {2, 6, 9}. Verification: I should be major (intervals 4, 3 from root). From 7: 7 to 11 = 4 semitones, 11 to 2 = 3 semitones. Major. IV from 0: 0 to 4 = 4, 4 to 7 = 3. Major. V from 2: 2 to 6 = 4, 6 to 9 = 3. Major. All three are major triads, which is correct for I, IV, and V in a major key. The progression in pitch classes: {7, 11, 2}, {0, 4, 7}, {2, 6, 9}, {7, 11, 2}.

**Worked Example 56.** Realize I-V-vi-IV in the key of (5, major). Scale from 5: 5, 7, 9, 10, 0, 2, 4. Degrees: 1st = 5, 2nd = 7, 3rd = 9, 4th = 10, 5th = 0, 6th = 2, 7th = 4. I = {5, 9, 0}: root 5, third 9 (4 semitones up), fifth 0 (3 more). Major. V = {0, 4, 7}: root 0, third 4 (4 semitones), fifth 7 (3 more). Major. vi = {2, 5, 9}: root 2, third 5 (3 semitones), fifth 9 (4 more). Minor. IV = {10, 2, 5}: root 10, third 2 (4 semitones), fifth 5 (3 more). Major. The progression: {5, 9, 0}, {0, 4, 7}, {2, 5, 9}, {10, 2, 5}.

Each of these progressions can be transposed to any of the twelve keys by adding a constant to every pitch class. The Roman numeral sequence stays the same. Only the PC content changes. This is one of the chief advantages of thinking in Roman numerals: a progression is a structural template, and the key fills in the specific pitches.

## VIII.C. The V-I Resolution

The resolution from V to I is the strongest gravitational pull in tonal music. Other resolutions exist, but none carries the same force. The reason is not cultural convention alone, though convention reinforces it. The reason is interval content.

In the key of 0, V7 = {7, 11, 2, 5}. This chord contains the tritone between PCs 11 and 5. Recall from Part II that the tritone (6 semitones) is the interval farthest from consonance, the point of maximum tension on the circle of Z₁₂. Within the context of a key, this particular tritone is special because its two notes are the leading tone (PC 11, scale degree 7) and the fourth degree (PC 5, scale degree 4). Both are tendency tones, pitch classes that the ear, trained by the key's hierarchy, expects to resolve in specific directions.

PC 11, the leading tone, sits one semitone below the tonic. The gap is as small as possible within the twelve-tone system. Melodically, a semitone gap between a note and a structural target creates a strong pull toward closure. PC 11 resolves upward by 1 to PC 0.

PC 5, the fourth degree, sits one semitone above the third of the tonic triad (PC 4). It resolves downward by 1 to PC 4.

Watch what happens to the tritone: {11, 5} resolves to {0, 4}. Both voices move by a single semitone, one ascending and one descending. The maximally dissonant interval (6 semitones) contracts to a major third (4 semitones), which is one of the most consonant intervals. Tension collapses into resolution in one step. This double-semitone resolution is the engine of tonal gravity.

Now consider the full voice leading from V7 to I. The four pitch classes of V7 are 7, 11, 2, and 5. Their natural resolution targets in I = {0, 4, 7} are:

- PC 7 stays as PC 7 (common tone: the root of V is the fifth of I)
- PC 11 moves up 1 to PC 0 (leading tone resolves to tonic)
- PC 2 moves down 2 to PC 0, or up 2 to PC 4 (both are members of I)
- PC 5 moves down 1 to PC 4 (fourth degree resolves to third)

The smoothest voice leading keeps PC 7 stationary, resolves 11 to 0 and 5 to 4 (both by semitone), and moves 2 to 0 (down 2) or 2 to 4 (up 2). Total voice-leading distance: 0 + 1 + 2 + 1 = 4 semitones of total motion. This is remarkably efficient. Four voices, four notes, and only four semitones of total displacement to move from maximum tension to complete resolution.

**Worked Example 57.** Trace the V7 to I resolution in the key of (3, major). Scale from 3: 3, 5, 7, 8, 10, 0, 2. V7 root = scale degree 5 = PC 10. V7 = {10, 2, 5, 8}. Check the tritone: PCs 2 and 8. Interval: (8 - 2) mod 12 = 6. Confirmed, that is a tritone. I = {3, 7, 10}. Resolution: PC 2 (leading tone of this key) moves up 1 to PC 3 (tonic). PC 8 (fourth degree of this key) moves down 1 to PC 7 (third of tonic triad). The tritone {2, 8} resolves to {3, 7}, a major third. PC 10 stays as PC 10 (common tone). PC 5 moves to PC 3 (down 2) or PC 7 (up 2). The pattern is the same in every key: both tendency tones converge by semitone, and the tritone resolves to the tonic triad's root and third.

The V to I motion is called an **authentic cadence** when it appears at the end of a phrase. When I is in root position and the melody ends on the tonic PC, it is a **perfect authentic cadence**, the strongest possible ending in tonal music. When the melody ends on the third or fifth rather than the tonic, or when I is in an inversion, it is an **imperfect authentic cadence**, still conclusive but with less finality. The terminology matters less than the mechanism: the tritone embedded in V7 resolves by semitone motion to the core of the tonic triad.

Other cadence types exist for comparison. A **half cadence** ends on V rather than resolving to I, creating the sensation of a musical comma rather than a period. A **plagal cadence** (IV to I) resolves without the dominant, producing a gentler, less urgent arrival. The plagal cadence is sometimes called the "Amen cadence" because of its association with hymn endings.[^46] A **deceptive cadence** (V to vi) substitutes vi for the expected I. Because vi shares two PCs with I (it is a tonic-function chord), the resolution partially satisfies the ear while simultaneously surprising it. The bass moves from V's root up to the sixth degree rather than down to the tonic, and the music continues where the listener expected it to stop.

## VIII.D. Circle Progressions

When chord roots move by descending fifths (equivalently, ascending fourths), the result is a circle progression. The name comes from the circle of fifths: each root step traces one position counterclockwise.

The full diatonic circle, starting from I and moving roots by descending fifths (subtracting 7, or equivalently adding 5, mod 12):

I (root 0) to IV (root 5) to vii° (root 11) to iii (root 4) to vi (root 9) to ii (root 2) to V (root 7) to I (root 0)

Verify the root motion: 0 + 5 = 5, 5 + 5 = 10... that gives root 10, which is not vii°. The pattern requires clarification. The root of each chord moves down by a fifth (subtracting 7 mod 12) from the previous chord: 0 - 7 = 5 (mod 12). Then 5 - 7 = 10, but the diatonic chord on scale degree 7 has root 11, not 10. Circle progressions in the diatonic context do not always produce exact fifths because the diatonic scale is not perfectly symmetric. Some "fifths" between diatonic roots are 7 semitones (perfect fifths) and one is 6 semitones (a diminished fifth, between the roots of IV and vii°). The sequence of roots by descending diatonic fifths (always staying within the scale) is: 0, 5, 11, 4, 9, 2, 7, 0. Each step moves to the scale degree a diatonic fifth below.[^47]

The most common segment of this circle is **ii to V to I**: roots 2, 7, 0. Each root descends by 7 (a perfect fifth) from the previous. This three-chord progression is the backbone of jazz harmony. It appears in hundreds of jazz standards, often repeated through multiple keys within a single piece.

In the key of 0 with seventh chords: ii7 = {2, 5, 9, 0}, V7 = {7, 11, 2, 5}, Imaj7 = {0, 4, 7, 11}. The voice leading from one chord to the next is remarkably smooth. From ii7 to V7: PC 2 stays (common tone), PC 5 stays (common tone), PC 9 moves down 2 to PC 7, PC 0 moves down 1 to PC 11. Only two voices move, and neither moves far. From V7 to Imaj7: PC 7 stays, PC 11 stays (becoming the major seventh of I), PC 2 moves down 2 to PC 0, PC 5 moves down 1 to PC 4. Again, two voices hold, two move minimally. This smooth voice leading is why the ii-V-I sounds so satisfying: the chords are different, but the transitions are gentle.[^48]

Longer circle segments extend the pattern. **vi to ii to V to I** (roots 9, 2, 7, 0) traces four steps counterclockwise. **iii to vi to ii to V to I** traces five. Each additional chord deepens the sense of harmonic momentum, because the ear perceives the recurring interval of a descending fifth as a pattern and anticipates its continuation. When V finally arrives at I, the resolution feels earned.

**Worked Example 58.** Trace a vi-ii-V-I circle progression in the key of (5, major). Scale from 5: 5, 7, 9, 10, 0, 2, 4. Triads: vi = {2, 5, 9} (root 2), ii = {7, 10, 2} (root 7), V = {0, 4, 7} (root 0), I = {5, 9, 0} (root 5). Root motion: 2 to 7 = +5 (up a fourth, equivalent to down a fifth mod 12). 7 to 0 = +5. 0 to 5 = +5. Each step adds 5, confirming the circle pattern. Verify chord qualities: vi has intervals 2 to 5 (3 semitones) and 5 to 9 (4 semitones), which is minor. ii has 7 to 10 (3) and 10 to 2 (4), minor. V has 0 to 4 (4) and 4 to 7 (3), major. I has 5 to 9 (4) and 9 to 0 (3), major. Qualities are minor, minor, major, major, matching the expected vi-ii-V-I pattern.

The circle of fifths, introduced in Part V as a way to organize keys, now reveals a second function: it organizes chord motion within a key. Root movement by fifth is the strongest type of harmonic motion, stronger than movement by third or by step. This is partly because the fifth is the most consonant non-octave interval (frequency ratio close to 3:2), and partly because two chords whose roots are a fifth apart share one pitch class (in triads) or two (in seventh chords), giving the transition both connection and contrast.

## VIII.E. Secondary Dominants

The seven diatonic chords provide a rich palette, but tonal music regularly steps outside the diatonic set for a specific purpose: to borrow the gravitational power of V7 and aim it at a chord other than I.

A secondary dominant is the V7 of some diatonic chord other than I. It is written V7/x, read "five-seven of x," where x is the target chord. The secondary dominant is not diatonic. It introduces one or two pitch classes from outside the key, creating a momentary flash of chromaticism that "points toward" its target. After the target chord arrives, the music returns to its original key as if nothing happened.

The construction is mechanical.

> **Algorithm: Build Secondary Dominant**
>
> **Input:** target chord root r (a pitch class within the current key)
>
> **Output:** the V7 chord that resolves to the target
>
> **Step 1.** Compute the dominant root: d = (r + 7) mod 12.
>
> **Step 2.** Build a dominant seventh chord on d: {d, (d + 4) mod 12, (d + 7) mod 12, (d + 10) mod 12}.

The output is always a major-minor seventh chord (dominant seventh type), regardless of the quality of the target chord. The secondary dominant borrows the leading-tone-to-root pull of V7 to I and redirects it toward a new target.

**Worked Example 59.** Build V7/V in the key of (0, major). The target is V, whose root is 7. Step 1: dominant root = (7 + 7) mod 12 = 2. Step 2: {2, 6, 9, 0}. This chord contains PC 6, which is not in the key of (0, major). In the diatonic set {0, 2, 4, 5, 7, 9, 11}, PC 6 is absent. The secondary dominant introduces it as a chromatic alteration, a raised fourth degree that serves as the leading tone of V. When {2, 6, 9, 0} resolves to V = {7, 11, 2}, the tritone within the secondary dominant ({6, 0}) resolves to {7, 11}, mirroring the standard tritone resolution of any V7 to its target I.

**Worked Example 60.** Build V7/vi in the key of (0, major). The target is vi, root 9. Dominant root: (9 + 7) mod 12 = 4. Chord: {4, 8, 11, 2}. Chromatic PC: 8, which is not in {0, 2, 4, 5, 7, 9, 11}. This is a raised fifth degree, acting as the leading tone of vi. Resolution: {4, 8, 11, 2} to vi = {9, 0, 4}. The tritone within the secondary dominant is {8, 2}: (2 - 8) mod 12 = 6. Confirmed. It resolves to {9, 0}, the root and seventh (well, in this case root and minor third) of the target.

**Worked Example 61.** Build V7/ii in the key of (0, major). Target is ii, root 2. Dominant root: (2 + 7) mod 12 = 9. Chord: {9, 1, 4, 7}. Chromatic PC: 1, absent from the diatonic set. This is a raised tonic degree, functioning as the leading tone of ii. Resolution: {9, 1, 4, 7} to ii = {2, 5, 9}.

Notice the pattern. Each secondary dominant introduces exactly one pitch class not found in the diatonic scale. That chromatic PC is always one semitone below the target's root, functioning as a temporary leading tone. This is what creates the tonicization: for the brief duration of the secondary dominant and its resolution, the target chord acts as a temporary tonic, complete with its own leading tone pulling toward it.

Secondary dominants can chain together. A common jazz pattern: V7/vi to vi to V7/ii to ii to V7/V to V to V7 to I. Each secondary dominant tonicizes the next chord, creating a cascade of resolutions that sweeps through the circle of fifths before landing on the true tonic. The key never actually changes. Each tonicization is local and fleeting. But the cumulative effect is a sense of harmonic richness far exceeding what the seven diatonic chords alone can provide.[^49]

There is one secondary dominant that cannot exist within the system: V7/vii°. The diminished triad is too unstable to function as a convincing temporary tonic. Its root supports a diminished fifth rather than a perfect fifth, so the resolution of a V7 chord to vii° sounds incomplete. In practice, the six remaining secondary dominants (V7/ii, V7/iii, V7/IV, V7/V, V7/vi, and, in minor keys, V7/VII) cover the useful cases.

## VIII.F. Common Progressions as Algorithms

The process of identifying chords within a key and labeling them with Roman numerals is called harmonic analysis. It is, at its core, pattern matching: given a chord (a set of pitch classes) and a key, determine which scale degree the chord is built on and what quality it has.

> **Algorithm: Roman Numeral Analysis**
>
> **Input:** a key (tonic t, scale type) and a sequence of chords, each given as a pitch-class set
>
> **Output:** a Roman numeral label for each chord
>
> **Step 1.** Build the scale from the key. Apply the step pattern from tonic t to generate the seven scale degrees.
>
> **Step 2.** Build all seven diatonic triads (and, if seventh chords are present, all seven diatonic seventh chords).
>
> **Step 3.** For each chord in the input sequence, compare its PC set to the diatonic triads/sevenths. If it matches, assign the corresponding Roman numeral.
>
> **Step 4.** If no diatonic match is found, check for secondary dominants: for each diatonic chord root r, compute the V7 of r and compare.
>
> **Step 5.** If still no match, check for borrowed chords (see section 8.G) or flag the chord as non-diatonic.

**Worked Example 62.** Analyze the chord sequence {9, 0, 4}, {5, 9, 0}, {0, 4, 7}, {7, 11, 2} in the key of (0, major).

Step 1: scale = {0, 2, 4, 5, 7, 9, 11}. Step 2: diatonic triads: I = {0, 4, 7}, ii = {2, 5, 9}, iii = {4, 7, 11}, IV = {5, 9, 0}, V = {7, 11, 2}, vi = {9, 0, 4}, vii° = {11, 2, 5}. Step 3: {9, 0, 4} = vi. {5, 9, 0} = IV. {0, 4, 7} = I. {7, 11, 2} = V. Result: **vi - IV - I - V**. All four chords are diatonic, and no secondary dominant check is needed.

**Worked Example 63.** Analyze {0, 4, 7}, {4, 8, 11}, {9, 0, 4}, {2, 5, 9}, {7, 11, 2, 5}, {0, 4, 7} in the key of (0, major).

Step 1-2: same as above, plus diatonic seventh chords: Imaj7 = {0, 4, 7, 11}, ii7 = {2, 5, 9, 0}, iii7 = {4, 7, 11, 2}, IVmaj7 = {5, 9, 0, 4}, V7 = {7, 11, 2, 5}, vi7 = {9, 0, 4, 7}, viiø7 = {11, 2, 5, 9}. Step 3: {0, 4, 7} = I. {4, 8, 11} is not among the diatonic triads (the diatonic triad on root 4 is {4, 7, 11}, but {4, 8, 11} has intervals 4 and 3 from root 4, making it a major triad on root 4, not minor). Move to Step 4: is {4, 8, 11} a secondary dominant? Check: V/vi would have root (9 + 7) mod 12 = 4. Build the triad on root 4 as a major chord: {4, 8, 11}. Match. This is V/vi (the triad portion of V7/vi). Continuing: {9, 0, 4} = vi. {2, 5, 9} = ii. {7, 11, 2, 5} = V7. {0, 4, 7} = I. Result: **I - V/vi - vi - ii - V7 - I**. The V/vi is a secondary dominant that tonicizes vi, and the remaining chords trace a circle progression (vi to ii to V to I) back home.

**Worked Example 64.** A sequence of triads is given in an unknown key: {3, 7, 10}, {8, 0, 3}, {1, 4, 8}, {3, 7, 10}. Determine the key and Roman numerals. Start by checking if the first chord could be I. If {3, 7, 10} is a major triad (intervals 4, 3), then the root is 3, and the key is (3, major). Scale from 3: {3, 5, 7, 8, 10, 0, 2}. Diatonic triads: I = {3, 7, 10}, ii = {5, 8, 0}, iii = {7, 10, 2}, IV = {8, 0, 3}, V = {10, 2, 5}, vi = {0, 3, 7}, vii° = {2, 5, 8}. Check: {8, 0, 3}, intervals from 8: 8 to 0 = 4, 0 to 3 = 3. Major triad on root 8. In our diatonic table, IV = {8, 0, 3}. Match. {1, 4, 8}: root is 1 (intervals 1 to 4 = 3, 4 to 8 = 4, so this is a minor triad on root 1). Root 1 is not a scale degree in (3, major). Step 4: check secondary dominants. V/ii would have root (5 + 7) mod 12 = 0. The major triad on root 0 is {0, 4, 7}, which does not match {1, 4, 8}. V/vi would have root (0 + 7) mod 12 = 7. Triad: {7, 11, 2}. No match. This chord is not a straightforward secondary dominant. It could be a borrowed chord. We revisit in the next section.

## VIII.G. Non-Functional Harmony

Not every chord in tonal music earns its place through functional logic. Some chords appear because the voice leading is beautiful, or because a composer borrowed them from a parallel mode, or because parallel motion in all voices creates a striking texture. These techniques expand the harmonic vocabulary beyond the diatonic set and the secondary dominants.

**Borrowed chords** (also called modal interchange) come from the parallel key. In the key of (0, major), the parallel minor is (0, natural minor), with the scale {0, 2, 3, 5, 7, 8, 10}. Any chord diatonic to (0, minor) can be borrowed into (0, major). The most commonly borrowed chords are:

The minor iv chord: {5, 8, 0}. The diatonic IV in major is {5, 9, 0}. The borrowed iv replaces PC 9 with PC 8, darkening the chord from major to minor. This substitution is ubiquitous in popular music. The progression I to IV to iv to I, where the major IV slides to a minor iv before resolving to I, creates a poignant quality that has been used in countless songs.[^50]

The flat-VII chord (written ♭VII): built on the lowered seventh degree of the major scale. In (0, major), the natural seventh degree is 11, but the minor scale has 10 as its seventh degree. ♭VII = {10, 2, 5}, a major triad. This chord has a rock-and-roll flavor, appearing in songs from the Beatles through modern alternative music. It does not resolve to I through leading-tone motion (it lacks the leading tone entirely), so its progression to I feels more like a slide than a resolution.

The flat-III chord (♭III): built on the lowered third degree. In (0, major): ♭III = {3, 7, 10}, a major triad. This chord is borrowed from the Aeolian mode (natural minor) and introduces PCs 3 and 10, neither of which belongs to the major scale. The sound is dramatic, a sudden shift to a foreign-sounding harmony that nevertheless resolves comfortably to diatonic chords.

The flat-VI chord (♭VI): {8, 0, 3}, a major triad on the lowered sixth degree. Its root is one semitone above the dominant (8 versus 7), creating a distinctive color. The progression ♭VI to ♭VII to I is common in film music and rock, moving the root up by whole step, then whole step, into the tonic. There is no traditional functional explanation for this motion. It works because of the stepwise root movement and the voice-leading connections between the chords.[^51]

**Chromatic voice leading** drives progressions where each voice moves by semitone regardless of harmonic function. A chromatic bass line descending from the tonic, 0, 11, 10, 9, can support a progression like I, V/vi (first inversion), IV (second inversion or a passing chord), I6. The bass creates a smooth line while the upper voices adjust to form consonant chords at each step. The logic is contrapuntal rather than functional: the line, not the function, determines the chord.

**Parallel motion** moves all voices by the same interval simultaneously. Parallel major triads ascending by whole step (say, {0, 4, 7} to {2, 6, 9} to {4, 8, 11}) produce a shimmering, non-functional effect. Strict classical counterpoint prohibits parallel fifths and octaves, but many genres, from Debussy's impressionism to modern film scoring, embrace parallel motion for its distinctive texture. In the integer system, parallel motion is simple to describe: apply T_n to the entire chord, where n is the step size.

These non-functional techniques do not replace the T-S-D-T framework. They coexist with it. A typical piece of tonal music might use functional progressions for most of its structure and introduce borrowed chords, chromatic lines, or parallel motion at key moments for color and surprise. The functional framework is the grammar. Non-functional harmony is the poetry.

# Part IX: TRANSPOSITION AND MODULATION

Transposition moves music to a new pitch level without changing its internal structure. Modulation changes the frame of reference itself, declaring a new tonic mid-piece. Both operations are central to tonal music, and both are remarkably clean in the integer system. Transposition reduces to addition. Modulation reduces to finding shared structure between two keys. This part formalizes both.

## IX.A. Transposition as Addition in Z₁₂

Transposition is the operation T_n, defined for any integer n in Z₁₂:

T_n(p) = (p + n) mod 12

Applied to a single pitch class, T_n shifts it n positions clockwise on the Z₁₂ circle. Applied to a melody (an ordered sequence of pitch classes), it shifts every element by n. Applied to a chord (an unordered set of pitch classes), it shifts every element by n. Applied to a scale, same thing. The operation is uniform: add n to everything.

The twelve transpositions have a clean algebraic structure. T_0 is the identity: adding 0 changes nothing. T_n composed with T_m equals T_{(n+m) mod 12}: transposing by n and then by m is the same as transposing by n + m. Every transposition has an inverse: the inverse of T_n is T_{12-n}, because (n + 12 - n) mod 12 = 0. These properties mean the set {T_0, T_1, T_2, ..., T_11} forms a group under composition, and that group is isomorphic to Z₁₂ itself. The same cyclic structure that organizes pitch classes also organizes the operations on them.

The defining property of transposition is that it **preserves all interval relationships**. If two pitch classes p and q are separated by an interval of d semitones, then T_n(p) and T_n(q) are also separated by d semitones. The proof is one line: ((q + n) - (p + n)) mod 12 = (q - p) mod 12 = d. Because every interval is preserved, the transposed version of a melody, chord, or scale sounds "the same but higher (or lower)." The relationships that give the music its character, the pattern of tension and release, the quality of the chords, the shape of the melody, survive transposition intact.

**Worked Example 65.** Transpose the melody [0, 4, 7, 4, 0] by T_5. Apply: [(0+5), (4+5), (7+5), (4+5), (0+5)] mod 12 = [5, 9, 0, 9, 5]. Verify intervals: original intervals between successive notes are (4-0) = 4, (7-4) = 3, (4-7) mod 12 = 9 (or equivalently, -3 mod 12 = 9 ascending, which is 3 descending), (0-4) mod 12 = 8 (or 4 descending). Transposed intervals: (9-5) = 4, (0-9) mod 12 = 3, (9-0) mod 12 = 9, (5-9) mod 12 = 8. Identical. The melodic shape is preserved exactly.

**Worked Example 66.** Transpose the C major triad {0, 4, 7} by T_3. Result: {3, 7, 10}. Internal intervals: 3 to 7 = 4 (major third), 7 to 10 = 3 (minor third), 3 to 10 = 7 (perfect fifth). These are the same intervals as in {0, 4, 7}: 0 to 4 = 4, 4 to 7 = 3, 0 to 7 = 7. The transposed chord is also a major triad. This must be the case, since transposition preserves all intervals, and chord quality is determined entirely by interval content.

This is the algebraic reason that all major triads sound alike (differing only in pitch level), all minor triads sound alike, and so on. Every major triad is a transposition of every other major triad. The set of all major triads is the orbit of {0, 4, 7} under the transposition group. Twelve starting points, twelve major triads, one interval structure.

## IX.B. Transposing Melodies and Chords

The practical motivation for transposition is simple. A singer whose comfortable range sits lower than the written melody needs the song in a lower key. A trumpet player reading a part written for clarinet needs to adjust for the different transposition of the two instruments. A composer who wants to repeat a theme in a new key applies transposition to the entire passage.

In the integer system, all of these operations reduce to a single instruction: add a constant to every pitch class. There is no need to reason about which notes gain sharps, which lose flats, or how the key signature changes. The constant is determined by the distance between the old key and the new key.

**Worked Example 67.** A melody is written in the key of (2, major): [2, 4, 6, 7, 9, 7, 6, 4, 2]. A singer needs it in the key of (9, major). The transposition interval is (9 - 2) mod 12 = 7. Apply T_7: [(2+7), (4+7), (6+7), (7+7), (9+7), (7+7), (6+7), (4+7), (2+7)] mod 12 = [9, 11, 1, 2, 4, 2, 1, 11, 9]. Every melodic interval is preserved. The song sounds identical to the original, just seven semitones higher.

In traditional notation, this transposition from D major to A major involves changing the key signature from two sharps to three sharps, rewriting every note on a different line or space of the staff, and checking for accidentals that need respelling. A student performing this task for the first time might spend ten minutes. In the integer system, it is one operation applied twelve times (once per note), each requiring a single addition mod 12. The mechanical simplicity is not a minor convenience. It eliminates an entire category of error.

Transposing a chord progression works the same way, but with an additional insight: **Roman numerals do not change under transposition**. The progression I-IV-V-I in the key of (0, major) is {0, 4, 7}, {5, 9, 0}, {7, 11, 2}, {0, 4, 7}. In the key of (5, major), it is {5, 9, 0}, {10, 2, 5}, {0, 4, 7}, {5, 9, 0}. The pitch classes are different; the Roman numerals are the same. This is because Roman numerals describe relationships to the tonic, and transposition preserves relationships. The entire harmonic structure is invariant.

**Transposing instruments** add one more layer. Certain instruments are built so that when the player reads and fingers a written C (PC 0 in the written part), the sounding pitch is something other than C. A B-flat clarinet sounds PC (p - 2) mod 12 when the written note is PC p. A horn in F sounds PC (p - 7) mod 12. An alto saxophone in E-flat sounds PC (p - 9) mod 12. In each case, the transposition is a fixed T_n applied to every note, and the integer framework handles it identically to any other transposition. The player's written part and the sounding result differ by a constant, nothing more.[^52]

**Worked Example 68.** A concert-pitch part has the melody [0, 4, 7]. A B-flat trumpet player needs to read notes that will sound as [0, 4, 7]. Since the trumpet transposes down by 2 (it sounds 2 semitones lower than written), the written part must be 2 semitones higher: T_2 applied to each note gives [2, 6, 9]. The player reads [2, 6, 9] and the instrument produces [0, 4, 7]. Transposing instruments are not mysterious. They apply a fixed T_n, and reversing the transposition recovers the original.

## IX.C. Common Modulation Techniques

Modulation changes the tonic. Unlike transposition, which shifts every pitch class uniformly while the tonic stays the same (relative to the music), modulation redefines which pitch class is home. A piece might begin in the key of (0, major), modulate to the key of (7, major) in its middle section, and return to (0, major) at the end. During the middle section, PC 7 is the tonic: all chord functions, tendency tones, and resolution targets are recalculated relative to PC 7.

This is a deeper operation than transposition. Transposition is arithmetic. Modulation is a change of coordinate system.

There are several standard techniques for modulating, each producing a different effect.

**Direct modulation** is the bluntest approach. The music simply begins behaving as though it is in a new key, often signaled by a V7 chord of the new key followed by the new tonic. In a direct modulation from (0, major) to (7, major), a D7 chord ({2, 6, 9, 0}, which is V7 in the key of 7) appears, resolves to {7, 11, 2}, and the new key is established. The transition can sound abrupt, which is sometimes the intent. Pop songs that shift up a half step or whole step for the final chorus almost always use direct modulation. The abruptness is the effect: a sudden lift of energy.[^53]

**Pivot chord modulation** is more subtle. A pivot chord is a chord that belongs to both the old key and the new key, though it has different Roman numeral labels in each. The music approaches the pivot chord as part of the old key, and the listener's ear accepts it in that context. After the pivot, the subsequent chords establish the new key, and the listener retroactively reinterprets the pivot chord in the new context. The transition feels smooth because the pivot chord belongs to both worlds.

**Chromatic modulation** uses chromatic voice leading (motion by semitone) to slide from one key to another. A single voice creeping up or down by half step can transform one chord into a chord from a distant key. The voice leading provides continuity, even when the keys are far apart on the circle of fifths.

**Enharmonic modulation** exploits the ambiguity of certain chord types. The fully diminished seventh chord, {0, 3, 6, 9}, divides the octave into four equal parts. Each of its four inversions is intervallically identical to the others (all internal intervals are minor thirds). This means a single diminished seventh chord can resolve as V7's upper tones in four different keys. Similarly, the augmented triad {0, 4, 8} divides the octave into three equal parts, making it reinterpretable in three keys.[^54] These symmetrical chords serve as modulatory wildcards, connecting keys that share no diatonic chords.

## IX.D. Pivot Chords

The pivot chord technique deserves its own algorithm, because finding pivot chords is a systematic, computable process.

> **Algorithm: Find Pivot Chords**
>
> **Input:** two keys, (tonic₁, type₁) and (tonic₂, type₂)
>
> **Output:** all chords diatonic to both keys, with their Roman numeral labels in each key
>
> **Step 1.** Build the seven diatonic triads for key 1. Label each with its Roman numeral.
>
> **Step 2.** Build the seven diatonic triads for key 2. Label each with its Roman numeral.
>
> **Step 3.** Compare the two lists. For each PC set that appears in both, record its Roman numeral in key 1 and its Roman numeral in key 2.

**Worked Example 69.** Find pivot chords between (0, major) and (7, major).

Key of (0, major) triads:
- I = {0, 4, 7}
- ii = {2, 5, 9}
- iii = {4, 7, 11}
- IV = {5, 9, 0}
- V = {7, 11, 2}
- vi = {9, 0, 4}
- vii° = {11, 2, 5}

Key of (7, major) scale: {7, 9, 11, 0, 2, 4, 6}. Triads:
- I = {7, 11, 2}
- ii = {9, 0, 4}
- iii = {11, 2, 6}
- IV = {0, 4, 7}
- V = {2, 6, 9}
- vi = {4, 7, 11}
- vii° = {6, 9, 0}

Now compare as unordered sets:

| PC set | In key of 0 | In key of 7 |
|:-------|:-----------:|:-----------:|
| {0, 4, 7} | I | IV |
| {7, 11, 2} | V | I |
| {9, 0, 4} | vi | ii |
| {4, 7, 11} | iii | vi |

Four pivot chords. These keys are one step apart on the circle of fifths (0 to 7 is one clockwise step), and they share four out of seven triads. This abundance of shared chords is why modulation to the dominant key sounds so natural: the music can slip into the new key through any of four doors.

Notice what changed: the pivot chord {0, 4, 7} functions as tonic (I) in the old key but becomes subdominant (IV) in the new key. The chord {7, 11, 2} was dominant (V) and becomes tonic (I). The functional reinterpretation is the heart of pivot chord modulation. The listener hears the chord in its old function, and only when the new key is established does the reinterpretation become clear.

**Worked Example 70.** Find pivot chords between (0, major) and (6, major). These keys are maximally distant (6 steps on the circle of fifths, the farthest possible).

Key of (6, major) scale: {6, 8, 10, 11, 1, 3, 5}. Triads:
- I = {6, 10, 1}
- ii = {8, 11, 3}
- iii = {10, 1, 5}
- IV = {11, 3, 6}
- V = {1, 5, 8}
- vi = {3, 6, 10}
- vii° = {5, 8, 11}

Compare with the key of (0, major) triads listed above. Searching for matches: {6, 10, 1} does not appear in key of 0. {8, 11, 3} does not appear. {10, 1, 5} does not. {11, 3, 6} does not. {1, 5, 8} does not. {3, 6, 10} does not. {5, 8, 11}: check against key of 0 triads. vii° in key of 0 is {11, 2, 5}. Not the same (the PC set {5, 8, 11} contains 8, which is not in {11, 2, 5}).

No common triads. Zero pivot chords.[^55] Keys that are 6 steps apart on the circle share no diatonic triads, which is why modulating between them requires chromatic or enharmonic techniques rather than a smooth pivot. The circle of fifths is not just a diagram. It is a map of modulatory difficulty.

**Worked Example 71.** Find pivot chords between (0, major) and (5, major) (one step counterclockwise, the subdominant direction).

Key of (5, major) scale: {5, 7, 9, 10, 0, 2, 4}. Triads:
- I = {5, 9, 0}
- ii = {7, 10, 2}
- iii = {9, 0, 4}
- IV = {10, 2, 5}
- V = {0, 4, 7}
- vi = {2, 5, 9}
- vii° = {4, 7, 10}

Compare with key of (0, major):

| PC set | In key of 0 | In key of 5 |
|:-------|:-----------:|:-----------:|
| {5, 9, 0} | IV | I |
| {0, 4, 7} | I | V |
| {9, 0, 4} | vi | iii |
| {2, 5, 9} | ii | vi |

Again, four pivot chords. One step counterclockwise yields the same count as one step clockwise. The symmetry is exact. In fact, the number of shared triads between two major keys depends only on their distance on the circle of fifths, not on the direction. Keys 1 step apart share 4 triads. Keys 2 steps apart share 3. Keys 3 steps apart share 2. The count decreases by one for each additional step, reaching zero at 6 steps (the tritone, the antipodal point on the circle).

This regularity is a consequence of the major scale's structure. Each clockwise step on the circle adds one new sharp (one PC changes), which eliminates one triad from the overlap and introduces one new one. The relationship is linear, and the circle of fifths is its organizing principle.

## IX.E. Modulation Distance

The concept of distance between keys, how "far apart" two keys feel, has a precise formulation in terms of the circle of fifths. The distance between two major keys with tonics t₁ and t₂ is the minimum number of steps between them on the circle:

d(t₁, t₂) = min((t₂ - t₁) mod 12 measured in fifths-steps, (t₁ - t₂) mod 12 measured in fifths-steps)

Equivalently, since each step on the circle of fifths corresponds to multiplying the PC difference by 7 (the generator), the distance in circle-of-fifths steps between t₁ and t₂ is the smallest k such that t₂ = (t₁ + 7k) mod 12 or t₂ = (t₁ - 7k) mod 12. In practice, the distance can be read directly from the circle diagram: count the shorter arc.

Close keys (1 to 2 steps) share many pitch classes and many pivot chords. Modulation between them is smooth, often imperceptible to a casual listener. A piece in the key of (0, major) modulating to (7, major) changes one pitch class (PC 5 is replaced by PC 6). A single chord is all it takes to pivot, and the new key feels like a natural extension of the old one.

Distant keys (4 to 6 steps) share few pitch classes and few or no pivot chords. Modulation between them requires more preparation: a chain of secondary dominants, a chromatic bass line, an enharmonic reinterpretation. The listener perceives the shift as dramatic, a significant change of scenery rather than a subtle adjustment.

The most common modulation targets in tonal music cluster around the close end of the spectrum:

**To the dominant key** (1 step clockwise). Tonic to (tonic + 7) mod 12. This is the most common modulation in Classical-era sonatas and concertos. The exposition states a theme in the home key, then modulates to the dominant for a second theme. The relationship is as close as two different keys can be.

**To the subdominant key** (1 step counterclockwise). Tonic to (tonic + 5) mod 12. The subdominant is the other "nearest neighbor" on the circle. Modulation to IV is common in the development sections of sonatas and in the B sections of many song forms.

**To the relative minor (or major)**. This modulation does not move on the circle of fifths at all in terms of key signature. The relative minor of (t, major) has tonic (t + 9) mod 12, and it shares all seven pitch classes with the major key. The distance in key-signature space is zero, though the tonal center shifts. This modulation is extremely smooth because no pitch classes change; only the hierarchy does. A phrase that begins sounding like C major (tonic 0) and gradually reorients around A minor (tonic 9) has undergone the gentlest possible modulation.

**To the parallel minor (or major)**. Same tonic, different mode. The key of (0, major) to (0, minor) keeps PC 0 as home but changes three pitch classes (as shown in Part IV, section 4.D). On the circle of fifths, parallel keys are 3 steps apart (the minor key is 3 positions counterclockwise from its parallel major). Despite this moderate distance, the shared tonic provides a strong anchor that makes the modulation feel coherent. The listener hears the same home note surrounded by a different landscape.

These four targets, dominant, subdominant, relative, and parallel, account for the majority of modulations in tonal music from the 17th through the 21st century. More distant modulations appear in Romantic-era music (Schubert was particularly fond of modulating by major third, which is 4 steps on the circle) and in jazz (where the ii-V-I pattern can be chained through distant keys within a few bars). But the close modulations are the bread and butter of the system.

The circle of fifths, first introduced in Part V as a generator of Z₁₂, has now appeared in three distinct roles: as the organizer of key signatures (Part V), as the pattern underlying circle progressions within a key (Part VIII), and as the map of modulatory distance between keys (here). These are not three separate applications of the same diagram. They are three facets of one algebraic fact: 7 and 12 are coprime, so repeated addition of 7 cycles through all 12 elements of Z₁₂. The circle of fifths is the geometric face of that arithmetic, and its ubiquity in music theory is a direct consequence of the coprimality of 7 and 12.

**Worked Example 72.** A jazz standard modulates from (0, major) through the following keys: (0, major) to (5, major) to (10, major) to (3, major) and back to (0, major). Compute the circle-of-fifths distance for each modulation. From 0 to 5: one step counterclockwise (subdominant direction). From 5 to 10: one step counterclockwise again. From 10 to 3: one step counterclockwise (10 + 5 = 15, mod 12 = 3). From 3 to 0: one step counterclockwise (3 + 5 = 8... that is not 0). Recalculate: from 3 to 0, the interval is (0 - 3) mod 12 = 9, and 9 in terms of fifths-steps: (3 + 7) mod 12 = 10, (3 + 14) mod 12 = 5, (3 + 21) mod 12 = 0. Three clockwise steps. So the return from (3, major) to (0, major) is a jump of 3 steps, while each of the prior modulations was only 1 step. This larger jump might be handled by a direct modulation or a chain of ii-V-I progressions cycling through the intermediate keys.

**Worked Example 73.** Determine the circle-of-fifths distance between (0, major) and (4, major). Count clockwise: 0 to 7 (1 step), 7 to 2 (2), 2 to 9 (3), 9 to 4 (4). Four steps clockwise. Count counterclockwise: 0 to 5 (1), 5 to 10 (2), 10 to 3 (3), 3 to 8 (4), 8 to 1 (5), 1 to 6 (6), 6 to 11 (7), 11 to 4 (8). Eight steps counterclockwise. The shorter path is 4 steps. These keys are moderately distant. They share 3 diatonic triads (by the count established in section 9.D) and differ in 4 pitch classes. Schubert's love of modulation by major third (4 semitones, which maps to 4 steps on the circle) produces a distinctive harmonic color: the keys are related enough to make sense in sequence but distant enough to sound surprising.

# Part X: RHYTHM, METER, AND DURATION

Everything so far has been about what to play. Pitch classes, scales, chords, keys, progressions: all of these describe which notes to select and how they relate to each other. None of them say anything about when. A chord is a set of pitch classes sounding simultaneously, but "simultaneously" presupposes time, and until now time has been invisible. This part makes it explicit.

A note has two independent properties. The first is pitch: which octave, which pitch class. The second is duration: how long the note sounds. Pitch lives in Z₁₂, a circular structure where 11 wraps back to 0. Duration lives on the positive real line, a purely linear structure where values stretch from infinitesimally short to arbitrarily long. These are mathematically distinct spaces. Pitch is cyclic. Duration is not. A pitch class of 13 is the same as a pitch class of 1, but a duration of 2 seconds is twice as long as a duration of 1 second, with no wraparound.

A complete note specification requires both dimensions: (octave, pitch class, duration), or more compactly, (note number, duration), written (n, d). A melody, then, is not merely an ordered sequence of pitch classes. It is an ordered sequence of (pitch class, duration) pairs, where each pair tells the performer what to play and how long to play it. Strip away the durations and the melody loses its rhythm. Strip away the pitch classes and the melody loses its tune. Both dimensions are necessary for music to exist as a temporal art rather than a static collection of frequencies.[^56]

## X.A. Beat, Pulse, and Tempo

A piece of music unfolds over time, and most music organizes that time around a regular pulse. The pulse is a series of evenly spaced time points, like the ticking of a clock. Each tick is a beat. Between any two adjacent beats, the same amount of time elapses.

Tempo measures how fast the beats arrive, expressed in beats per minute (BPM). At 60 BPM, one beat arrives every second. At 120 BPM, two beats per second. At 40 BPM, one beat every 1.5 seconds. The conversion is straightforward: the duration of one beat in seconds equals 60 / BPM. A tempo of 90 BPM gives beats spaced 60/90 = 2/3 of a second apart.

The beat is to time what the semitone is to pitch: the fundamental reference unit. Just as all intervals are measured in semitones, all durations are measured in beats (or fractions of beats). A note lasting two beats is twice as long as a note lasting one beat. A note lasting half a beat sits halfway between two consecutive pulse points. The beat provides the grid against which every rhythmic event is located.

This grid is an idealization. Real performance deviates from strict regularity for expressive purposes, a practice called rubato. A pianist might linger on an important note, arriving at the next beat slightly late, then compress the following notes to catch up. A conductor might stretch the final phrase of a movement, slowing the tempo gradually to signal closure. These deviations are meaningful precisely because the listener perceives them against the background of regular pulse. Without the expectation of regularity, there is nothing to deviate from. Rubato is expression measured against a norm, the same way chromaticism is color measured against a key.[^57]

Some music abandons regular pulse entirely. Free-time passages, cadenzas in concertos, certain passages in contemporary art music: these exist outside the beat grid. They are the rhythmic equivalent of atonality, and like atonality, they define themselves in part by what they reject.

## X.B. Meter and Time Signatures

A beat is a single point in time. Meter groups beats into recurring patterns of strong and weak, giving the pulse a shape that the listener feels as a regular cycle.

The simplest way to understand meter is through the time signature, the two stacked numbers that appear at the beginning of a score. The top number specifies how many beats fill one measure (also called a bar). The bottom number specifies which note value receives one beat. The measure is the meter's repeating unit: a fixed-length container that cycles over and over, each iteration carrying the same pattern of strong and weak beats.

**4/4 time** is the most common meter in Western music. Four quarter-note beats per measure. The stress pattern is strong, weak, medium, weak. Beat 1 carries the primary accent, the downbeat. Beat 3 carries a secondary accent, less pronounced than beat 1 but stronger than beats 2 and 4. This four-beat cycle underpins the vast majority of pop, rock, folk, classical, and jazz repertoire. Its dominance is so total that it is sometimes called "common time" and marked with a C symbol rather than a fraction.

**3/4 time** has three quarter-note beats per measure. The stress pattern is strong, weak, weak. This is the meter of the waltz: a repeating cycle of one accented beat followed by two unaccented ones, producing the characteristic "OOM-pah-pah" that propels dancers in circles. The three-beat cycle feels fundamentally different from the four-beat cycle. Music in 3/4 has a lilt, a forward momentum driven by the asymmetry of dividing time into groups of three rather than the more balanced groups of four.

**2/4 time** has two quarter-note beats: strong, weak. This is the meter of the march. Two beats per cycle, left foot, right foot, with the downbeat on beat 1 providing a regular accent for stepping.

These three meters, 2/4, 3/4, and 4/4, are all **simple meters**. In a simple meter, each beat divides naturally into two equal parts. A quarter-note beat in simple time splits into two eighth notes. Each eighth note occupies half a beat.

**Compound meters** work differently. In a compound meter, each beat divides naturally into three equal parts. The time signature looks different because the note value receiving "one beat" is a dotted note rather than a plain one.

6/8 is the most common compound meter. The top number, 6, counts eighth notes per measure. But the performer does not feel six separate beats. Instead, the six eighths group into two dotted-quarter-note beats (each dotted quarter spanning three eighths). The stress pattern is strong-weak-weak, medium-weak-weak: two main beats, each subdividing into three. 9/8 works similarly, grouping nine eighths into three dotted-quarter beats. 12/8 groups twelve eighths into four dotted-quarter beats.

The distinction between 6/8 and 3/4 deserves attention because both meters contain exactly six eighth notes per measure. The total duration is the same. The difference is internal grouping. 3/4 groups those six eighths as THREE groups of TWO: (12)(34)(56). 6/8 groups them as TWO groups of THREE: (123)(456). A conductor in 3/4 gives three beats per bar. A conductor in 6/8 gives two. Same duration, different skeleton. The musical effect is unmistakable. 3/4 has a waltz feel. 6/8 has a rolling, lilting quality, common in jigs, barcarolles, and much folk music.

**Asymmetric meters** (also called irregular or odd meters) cannot be divided into equal groups of two or three. 5/4 contains five quarter-note beats, typically grouped as 3+2 or 2+3. The grouping matters and must be specified, because 3+2 and 2+3 produce different stress patterns. Dave Brubeck's "Take Five" uses 3+2, giving it a distinctive swing between a three-beat group and a two-beat group.[^58] 7/8 groups seven eighth notes, often as 2+2+3, 3+2+2, or 2+3+2. Bulgarian folk music and progressive rock both favor 7/8, though with very different aesthetics.

The general principle: any positive integer can serve as the top number of a time signature, and any power of 2 as the bottom number. The top number says how many. The bottom says how many of what. The two together define the measure's size and internal unit.

## X.C. Note Durations as Fractions

In most Western notation, the whole note serves as the reference unit for duration. Every other standard duration is a power-of-two fraction of a whole note:

| Duration name | Fraction of whole note | Symbol |
|:---|:---:|:---:|
| Whole note | 1 | |
| Half note | 1/2 | |
| Quarter note | 1/4 | |
| Eighth note | 1/8 | |
| Sixteenth note | 1/16 | |
| Thirty-second note | 1/32 | |

The pattern is a binary tree. Each level halves the previous duration. In general, the k-th level has duration 1/2^k, where k = 0 for the whole note, k = 1 for the half, k = 2 for the quarter, and so on.

**Dots** modify a note's duration by adding half its value. A dotted half note = 1/2 + 1/4 = 3/4 of a whole note. A dotted quarter = 1/4 + 1/8 = 3/8. A dotted eighth = 1/8 + 1/16 = 3/16. The formula for a single dot: dotted duration = d + d/2 = 3d/2, where d is the undotted value. A double dot adds another quarter of the original: d + d/2 + d/4 = 7d/4. A double-dotted half note = 1/2 + 1/4 + 1/8 = 7/8.

The dot operation has a clean fractional structure. Each additional dot adds the next power of 1/2 of the original duration. With n dots, the total duration is d × (2^(n+1) - 1) / 2^(n+1). In practice, single dots are common, double dots are occasional, and triple dots are rare enough to ignore.

**Ties** connect two notes of the same pitch, combining their durations into a single sustained sound. A half note tied to a quarter note sounds for 1/2 + 1/4 = 3/4 of a whole note. Any rational duration can be constructed by tying together standard note values. A note lasting 5/8 of a whole note? Tie a half note (4/8) to an eighth note (1/8). A note lasting 7/16? Tie a quarter (4/16) to a dotted eighth (3/16). Ties are the escape valve from the binary-only system of note values: they allow the construction of arbitrary durations from standard building blocks.

**Rests** are silences. Each note duration has a corresponding rest of the same length: whole rest (1), half rest (1/2), quarter rest (1/4), and so on. A rest occupies time without producing sound. In the (n, d) framework, a rest has a duration but no pitch: it could be written (silence, d).

The arithmetic of filling a measure is straightforward. In 4/4 time, each measure contains exactly 1 whole note's worth of duration: 4 × 1/4 = 1. Any combination of notes and rests whose durations sum to 1 fills a measure completely. Four quarter notes: 1/4 + 1/4 + 1/4 + 1/4 = 1. Two half notes: 1/2 + 1/2 = 1. One half note, one quarter note, two eighth notes: 1/2 + 1/4 + 1/8 + 1/8 = 1. One dotted half note and one quarter note: 3/4 + 1/4 = 1.

**Worked Example 74.** In 3/4 time, how much total duration fills one measure? Three quarter notes: 3 × 1/4 = 3/4 of a whole note. Verify: a dotted half note also equals 3/4, so a single dotted half fills a bar of 3/4 exactly. Now fill a measure of 3/4 with the following combination: one quarter note, one eighth note, one eighth note, one quarter note. Total: 1/4 + 1/8 + 1/8 + 1/4 = 1/4 + 1/4 + 1/4 = 3/4. The measure is complete.

**Worked Example 75.** In 6/8 time, each measure holds 6 × 1/8 = 6/8 = 3/4 of a whole note. A dotted quarter note equals 1/4 + 1/8 = 3/8. Two dotted quarters fill a measure: 3/8 + 3/8 = 6/8 = 3/4. This confirms the compound-meter interpretation: 6/8 has two beats, each a dotted quarter long, totaling 3/4 of a whole note per measure, the same total duration as a measure of 3/4 simple time.

## X.D. Tuplets and Subdivision

Standard subdivisions follow powers of 2. A quarter note splits into two eighths. An eighth splits into two sixteenths. The subdivision tree is strictly binary: every level doubles the number of notes and halves their duration.

Tuplets override this binary default by fitting a non-power-of-2 number of notes into a space designed for a power-of-2 number.

The most common tuplet is the **triplet**: three notes in the space of two. An eighth-note triplet fits three notes into the span of one quarter note (the space normally occupied by two eighth notes). Each triplet note lasts 2/3 of an eighth note. Since an eighth note is 1/8 of a whole note, each triplet eighth is (2/3) × (1/8) = 1/12 of a whole note. Three of them total 3 × 1/12 = 3/12 = 1/4, filling exactly one quarter note's worth of time.

The triplet introduces a factor of 3 into an otherwise binary system. Where the standard subdivision tree produces only durations of the form 1/2^k, the triplet generates 1/12, a duration that cannot be expressed as any power-of-two fraction. This is why triplets sound distinctive: they carve time into divisions that the underlying meter does not anticipate.

A **quintuplet** fits 5 notes into the space of 4 (or sometimes 2). Five sixteenth-note quintuplets in the space of four sixteenths give each note a duration of (4/5) × (1/16) = 4/80 = 1/20. A **septuplet** fits 7 into the space of 4 (or 8, depending on context), and so on.

The general formula: an n-tuplet in the space of m standard subdivisions, where each standard subdivision has value s, gives each tuplet note a duration of (m × s) / n. The total duration of all n notes is n × (m × s) / n = m × s, confirming that the tuplet fills exactly the space of m standard notes.

**Worked Example 76.** A quarter-note triplet fits three notes into the space of two quarter notes (one half note). Each triplet quarter note lasts (2 × 1/4) / 3 = 2/12 = 1/6 of a whole note. Three of them: 3 × 1/6 = 1/2. They fill one half note exactly. In a measure of 4/4, a quarter-note triplet occupies half the bar, and the remaining half must be filled by notes or rests totaling 1/2.

**Worked Example 77.** A quintuplet of sixteenth notes spans the space normally occupied by four sixteenth notes (one quarter note). Each note: (4 × 1/16) / 5 = 4/80 = 1/20 of a whole note. Five of them: 5 × 1/20 = 1/4. The quintuplet fills one beat in 4/4 time.

Nested tuplets are possible but increasingly rare. A triplet of triplets, three triplet notes in the space of two triplet notes, introduces a factor of 9 into the subdivision. The result is nine notes in the space of four standard subdivisions, each lasting 4/(9 × s). Composers like Brian Ferneyhough and Elliott Carter use nested tuplets to create rhythmic textures of extreme complexity, but in most practical music, single-level triplets are the limit of subdivision complexity.[^59]

## X.E. Syncopation and Displacement

Every meter carries a built-in hierarchy of strong and weak beats. In 4/4, beat 1 is strongest, beat 3 is next, beats 2 and 4 are weakest. Each beat further subdivides: the downbeat half of a beat is stronger than the upbeat half. This hierarchy is the metric grid, the rhythmic equivalent of a key's tonal hierarchy.

Syncopation places accents where the grid does not expect them. A note that arrives on a weak beat, or between beats, and receives emphasis through loudness, duration, or harmonic change, contradicts the meter's default stress pattern. The contradiction creates rhythmic tension, a pull between what the ear expects and what actually happens.

Several mechanisms produce syncopation:

**Anticipation** shifts a note earlier than expected. Instead of sounding on beat 1, the note arrives on the "and" of beat 4 in the preceding measure (half a beat early) and sustains through the downbeat. The ear hears the accent displaced forward in time. The effect is eagerness, a sense that the music cannot wait for the beat to arrive.

**Delayed attack** shifts a note later than expected. Beat 1 passes in silence (or with a tie from a previous note), and the new note enters on the "and" of beat 1. The downbeat is present in the listener's mental grid but absent in the sound. The gap creates a momentary suspension before the note arrives.

**Missed downbeat** is the strongest form of syncopation: the strong beat is occupied by a rest, and the accent falls on a following weak beat. In 4/4, a rest on beat 1 followed by a note on beat 2 forces the listener to feel the accent in the "wrong" place. Reggae uses this systematically, placing the guitar or keyboard attack on beats 2 and 4 while beat 1 is left open, producing the characteristic offbeat feel.

Mathematically, syncopation is a phase shift. The rhythmic pattern is displaced by a fraction of a beat relative to the metric grid. If the grid places strong beats at positions 0, 1, 2, 3 (measured in beats), a syncopated pattern might place its attacks at positions 0.5, 1.5, 2.5, 3.5, exactly half a beat off the grid. The pattern itself might be perfectly regular, but its alignment with the meter is shifted. The displacement creates the tension.

This is structurally parallel to harmonic dissonance. A dissonant interval derives its tension from the listener's expectation of consonance, an expectation set by the key. A syncopated rhythm derives its tension from the listener's expectation of the downbeat, an expectation set by the meter. In both cases, the effect depends on a norm. Syncopation without meter is meaningless, the way a tritone without a key is merely an interval rather than a dissonance.[^60]

**Worked Example 78.** Consider a measure of 4/4 with the following attack pattern (where x marks a note onset and . marks a continuation or rest):

Beat:     1   &   2   &   3   &   4   &
Pattern:  .   x   .   x   .   x   .   x

Every attack falls on an upbeat (the "and" of each beat). No downbeat receives an attack. This is a fully syncopated pattern. Each note anticipates the following beat by half a beat. The pattern is regular (evenly spaced), but its phase is shifted by 1/2 beat from the metric grid. Against a bass line or drum pattern that marks the downbeats, this syncopation creates the push-pull feel characteristic of funk and certain jazz styles.

## X.F. Polyrhythm and Polymeter

When two or more simultaneous voices use different rhythmic subdivisions, the result is polyrhythm. When they use different meters, it is polymeter. Both create textures in which multiple time-organizing principles coexist.

The simplest and most pervasive polyrhythm is **3-against-2** (sometimes called hemiola). One voice divides a span of time into three equal parts while another divides the same span into two. If the total span is 1 (one whole note), one voice places attacks at 0, 1/3, and 2/3, while the other places attacks at 0 and 1/2.

To find when the two voices align, think of the span as subdivided into lcm(3, 2) = 6 equal parts. Voice A (triplet) attacks on subdivisions 0, 2, 4. Voice B (duplet) attacks on subdivisions 0, 3. The only coincidence point is subdivision 0 (the downbeat). Between coincidences, the two patterns interleave:

| Subdivision | 0 | 1 | 2 | 3 | 4 | 5 |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|
| Voice A (÷3) | x | | x | | x | |
| Voice B (÷2) | x | | | x | | |
| Combined | x | | x | x | x | |

The combined pattern, x . x x x ., has an irregular quality that neither voice produces alone. The 3-against-2 polyrhythm is fundamental to West African drumming, Afro-Cuban music, and their descendants in jazz, blues, and popular music worldwide.

**Worked Example 79.** Trace a 4-against-3 polyrhythm. The total span: 1. Voice A divides into 4 equal attacks: 0, 1/4, 1/2, 3/4. Voice B divides into 3 equal attacks: 0, 1/3, 2/3. The minimal common grid has lcm(4, 3) = 12 subdivisions. Voice A attacks on subdivisions 0, 3, 6, 9 (each separated by 12/4 = 3). Voice B attacks on subdivisions 0, 4, 8 (each separated by 12/3 = 4).

| Sub | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| A (÷4) | x | | | x | | | x | | | x | | |
| B (÷3) | x | | | | x | | | | x | | | |
| Combined | x | | | x | x | | x | | x | x | | |

The two voices coincide only at subdivision 0. Between coincidences, the pattern has a complexity that neither voice produces alone. The ear struggles to assign a single "correct" subdivision, and this perceptual ambiguity is what gives polyrhythm its distinctive tension.

**Polymeter** is a different phenomenon. In polyrhythm, both voices share the same beat and the same total span but subdivide it differently. In polymeter, the two voices operate in different meters entirely: one might play in 3/4 while another plays in 4/4, each with its own measure length. The downbeats align at the start and then diverge, not coinciding again until lcm of the two measure lengths has elapsed.

**Worked Example 80.** Two voices play simultaneously, one in 3/4 and one in 4/4, at the same tempo (same quarter-note pulse). Voice A in 3/4 has a downbeat every 3 beats. Voice B in 4/4 has a downbeat every 4 beats. The downbeats coincide every lcm(3, 4) = 12 beats. After the initial downbeat, Voice A's downbeats fall at beats 1, 4, 7, 10, 13... Voice B's fall at beats 1, 5, 9, 13... They realign at beat 13, which is both Voice A's 5th downbeat and Voice B's 4th. The 12-beat span between coincidences is the polymetric cycle. Within that cycle, the two voices create a texture of shifting accents as their respective downbeats slide past each other.

The lcm function appeared earlier in the context of pitch (the circle of fifths is generated by repeated addition of 7, and 7 and 12 are coprime, so lcm(7, 12) = 84 determines certain properties of the system). Here it reappears in rhythm, governing when simultaneous patterns converge. The same arithmetic underlies both domains. Pitch and rhythm are different physical dimensions of music, but their mathematical structures share common tools.[^61]

More complex polyrhythms scale the same principle. 5-against-3: lcm(5, 3) = 15 subdivisions, coincidence only at position 0. 5-against-4: lcm(5, 4) = 20. 7-against-4: lcm(7, 4) = 28. As the numbers grow coprime and large, the patterns become longer before repeating, and the perceptual effect becomes increasingly dense. West African drum ensembles and composers like Conlon Nancarrow have explored these textures to extraordinary depth, building entire compositions around the interplay of cycles that align only at long intervals.

---

# Part XI: FORM AND STRUCTURE

A note is a point. A phrase is a line. A piece is an architecture. Everything discussed so far, pitch classes, scales, chords, progressions, rhythm, operates at the local level, governing what happens from beat to beat and measure to measure. Form operates at a higher level, organizing phrases into sections and sections into complete works. Where harmony asks "what chord comes next?", form asks "what happens next in the large-scale plan?"

Form is not ornamental. It is the reason a three-minute pop song feels complete and a five-second random sequence of chords does not. The listener may not consciously track the form, but the form creates the expectations that give the music its arc: departure, contrast, return, resolution. These are the same forces that drive harmonic progressions (T to S to D to T), now operating on a larger time scale.

## XI.A. Phrases, Periods, and Sentences

The phrase is the smallest complete musical thought. It is the musical equivalent of a sentence in prose: a unit with a beginning, a middle, and an end. What makes the end an end, rather than a pause, is the cadence. The cadence types from Part VIII (authentic, half, plagal, deceptive) serve as the punctuation marks that close phrases. An authentic cadence (V to I) is a period: full stop. A half cadence (ending on V) is a comma: the thought pauses but does not conclude.

Most phrases in tonal music span 4 or 8 measures, though this is a strong tendency rather than a rule. The 4-measure phrase is deeply embedded in Western musical grammar, so much so that listeners perceive deviations from it (phrases of 3, 5, or 7 measures) as asymmetric or surprising. Phrase length is one of the simplest structural expectations a listener carries, and composers manipulate it for effect: extending a phrase past its expected endpoint creates suspense, while truncating one creates urgency.

Two phrases can combine into larger structures. A **period** pairs two phrases in an antecedent-consequent relationship. The antecedent phrase ends with a half cadence (on V), posing a musical question. The consequent phrase, often beginning with similar or identical material, ends with an authentic cadence (on I), providing the answer. The two phrases together form a complete thought that neither could form alone. The antecedent creates an expectation of continuation. The consequent fulfills it.

**Worked Example 81.** A period in the key of (0, major). The antecedent phrase (4 measures) uses the progression I, IV, I, V, ending with a half cadence on V = {7, 11, 2}. The consequent phrase (4 measures) begins with the same I chord, diverges through ii, V7, and resolves to I = {0, 4, 7} with an authentic cadence. The antecedent asks. The consequent answers. The period spans 8 measures total, and the harmonic motion from "ending on V" to "ending on I" gives the whole structure a sense of departure and return.

A **sentence** is a different 8-measure structure. It begins with a short idea, typically 2 measures long, called the basic idea. The basic idea is then repeated or varied in the next 2 measures (the repetition). The final 4 measures form the continuation, which develops the material and drives toward a cadence. The proportions are 1:1:2 (2 + 2 + 4 measures). Where a period derives its structure from the question-answer relationship between two cadences, a sentence derives its structure from the presentation-then-development of a single idea.

**Worked Example 82.** A sentence in the key of (7, major). Basic idea (measures 1-2): a melodic fragment over I = {7, 11, 2} moving to V = {2, 6, 9}. Repetition (measures 3-4): the same fragment transposed up, or the same fragment with altered rhythm, over I moving to IV = {0, 4, 7}. Continuation (measures 5-8): the rhythmic activity increases, the harmony moves through ii = {9, 0, 4} and V7 = {2, 6, 9, 0}, and the phrase concludes with an authentic cadence on I. The 2+2+4 structure is audible even without conscious analysis: the listener hears an idea stated twice, then developed and resolved.

These building blocks, phrases, periods, and sentences, are the atoms from which larger forms are assembled. A binary form is two phrases (or groups of phrases). A sonata is dozens of phrases organized into three large sections. The same way chords are built from pitch classes and progressions from chords, musical forms are built from phrases.

## XI.B. Binary Form (AB)

Binary form divides a piece into two sections, A and B, each typically repeated. The structure is ||: A :||: B :||, where the double bars and repeat signs indicate that each section is played twice.

Section A establishes the home key and presents the primary melodic material. In many binary-form pieces, A modulates at its end, arriving at a cadence in the dominant key (for major-key pieces) or the relative major (for minor-key pieces). The move away from home is what makes A feel incomplete. It opens a harmonic arc that B must close.

Section B begins in the new key and gradually works back to the home key, arriving with an authentic cadence. The return home provides the structural closure that A's departure denied. B often uses the same melodic material as A, transformed or developed, but this is not required. The essential feature of binary form is the key scheme: departure in A, return in B.

In pitch-class terms: if the home key is (t, major), A ends on a chord from the key of (t + 7, major), the dominant. B navigates back through the circle of fifths and resolves to (t, major). The tonal journey is an arc, starting and ending at the same point.

Many Baroque dance movements use binary form. Minuets, gavottes, bourrees, allemandes, courantes: the dance suites of Bach, Handel, and their contemporaries are catalogues of binary form in different meters and characters. Each dance is a two-section structure with repeats, and the harmonic plan follows the departure-and-return template.[^62]

**Worked Example 83.** A binary-form minuet in the key of (5, major). Section A (8 measures): begins on I = {5, 9, 0}, progresses through diatonic chords, and cadences on V in the key of (0, major), landing on {0, 4, 7} as a new tonic. Section B (8 measures): begins with material in the key of (0, major), modulates back through a circle progression (vi to ii to V to I in the key of 5), and concludes with a perfect authentic cadence on I = {5, 9, 0}. The repeat signs mean the listener hears A twice, then B twice: AABB. The double hearing reinforces both the departure and the return.

## XI.C. Ternary Form (ABA)

Ternary form has three sections: A, a contrasting B, and a return of A. The fundamental difference from binary is the return. In binary form, B continues from where A left off, and the material is often closely related. In ternary form, B is genuinely contrasting, often in a different key, tempo, or character, and A comes back, providing the satisfaction of hearing familiar material after a departure.

The return of A may be exact, in which case the score simply marks "D.C." (da capo, "from the head"), directing the performer back to the beginning. Or the return may be varied, with the original material ornamented, re-harmonized, or otherwise altered. Either way, the structural point is the same: the listener hears A, leaves it for B, and comes home.

Ternary form nests. Each section can internally have its own form. An A section might itself be a binary form. A B section might be a sentence. This nesting creates layers of structure, forms within forms, all organized by the principle of statement, contrast, and return.

The most familiar ternary form in classical music is the minuet and trio. The minuet (A) is typically a binary form in the home key. The trio (B) is another binary form, often in a contrasting key (the subdominant, the relative minor, or the parallel minor). After the trio, the minuet returns, usually without repeats: A B A. The scherzo and trio in later Classical and Romantic symphonies follows the same plan at a faster tempo and with more rhythmic energy.

**Worked Example 84.** A ternary form in the key of (9, major). A section (16 measures): a period (antecedent + consequent) in (9, major), followed by a second period, all within the home key. B section (16 measures): contrasting material in the key of (4, major), the dominant. A section returns (16 measures): the same material as the original A, back in (9, major). The key scheme, (9) to (4) to (9), creates a departure-and-return arc at the section level, mirroring the phrase-level arcs created by half cadences and authentic cadences.

## XI.D. Rondo (ABACA...)

Rondo form is built on the principle of recurrence. A main theme (the refrain, or A section) alternates with contrasting episodes (B, C, D...). The refrain returns after each episode, always in the home key. The simplest rondo: ABACA. More elaborate patterns: ABACABA, or ABACADA.

The structure can be modeled as a function from section position to thematic material:

- Odd-numbered sections (1st, 3rd, 5th, ...) present the refrain A, always in the tonic key.
- Even-numbered sections (2nd, 4th, ...) present contrasting episodes, typically in different keys.

The refrain's recurrence exploits a deep principle of musical perception: the pleasure of recognition. Each time A returns, the listener recognizes familiar material, and this recognition is satisfying in proportion to the intervening contrast. The episodes create distance from A, making each return feel like an arrival. The rondo is, in this sense, a form built on nostalgia: each departure sets up the gratification of coming home.

**Worked Example 85.** An ABACA rondo in the key of (0, major). A (8 measures): theme in I, ending with an authentic cadence. B (8 measures): contrasting episode in the key of (7, major), the dominant. A returns (8 measures): theme in I, identical or nearly identical to the first A. C (8 measures): contrasting episode in the key of (9, minor), the relative minor. A returns (8 measures): theme in I, concluding the piece. The key scheme, (0) to (7) to (0) to (9, minor) to (0), creates a pattern of increasingly distant departures with consistent returns. Each return to (0, major) reaffirms the tonic.

Each episode typically visits a different key, giving the form a palette of harmonic colors unified by the refrain's constant return to the tonic. In a five-part rondo (ABACA), the B episode might visit the dominant while the C episode visits the subdominant or the relative minor. In a seven-part rondo (ABACABA), the additional episodes push further afield, making the final return of A all the more satisfying for the distance traveled.

## XI.E. Sonata-Allegro Form

Sonata-allegro form (usually just called "sonata form") is the most elaborate standard form in Western tonal music. It dominated the first movements of symphonies, concertos, sonatas, and chamber works from roughly 1750 through 1900, and its influence extends into the present. Where binary and ternary forms organize material around simple departure and return, sonata form turns the relationship between keys into a dramatic argument.

The form has three main sections: exposition, development, and recapitulation.

The **exposition** introduces two contrasting theme groups. Theme group 1 is presented in the tonic key. A transitional passage (the bridge) modulates to a new key, and theme group 2 is presented there. For major-key sonatas, the second key is almost always the dominant (tonic + 7 mod 12). For minor-key sonatas, the second key is typically the relative major (tonic + 3 mod 12). The exposition is often repeated, giving the listener two hearings of this crucial material.

The tonal split is the structural crux. By presenting two themes in two different keys, the exposition creates a tension that requires resolution. The music has established two tonal centers, and the listener senses, consciously or not, that this duality cannot persist. The rest of the form exists to resolve it.

The **development** section takes the themes introduced in the exposition and subjects them to transformation. Themes are fragmented, combined in new ways, transposed to remote keys, varied in rhythm and texture. The harmonic landscape is unstable: the music wanders through keys distant from both the tonic and the dominant, often tracing extended passages through the circle of fifths. Where the exposition was tonally stable (settled in two clearly defined keys), the development is tonally restless.

**Worked Example 86.** The exposition of a sonata in (0, major). Theme 1: a sentence in I, 8 measures, establishing the tonic key with the progression I, V, I, IV, ii, V7, I. Bridge: 4 measures modulating from (0, major) to (7, major) through a pivot chord (the chord {0, 4, 7}, which is I in the home key and IV in the new key). Theme 2: a period in the key of (7, major), 8 measures, using the progression I = {7, 11, 2}, IV = {0, 4, 7}, V = {2, 6, 9}, I. The two themes now stand in two different keys, separated by a fifth on the circle. Closing material: 4 measures confirming (7, major). Total exposition: 24 measures, tonally split between (0) and (7).

The **recapitulation** restates both theme groups, but with a critical difference: theme group 2, which appeared in the dominant key during the exposition, now returns in the tonic key. The duality is resolved. What was harmonically split is unified. The bridge passage is rewritten (or omitted) so that the music stays in the home key throughout.

This is the structural argument of sonata form. The exposition poses a tonal question: two themes, two keys. The development explores the implications of that split, destabilizing both themes. The recapitulation answers the question: both themes, one key. The music has traveled and returned, and the return settles the harmonic tension that the exposition introduced.

A **coda** may follow the recapitulation, providing additional closing material that confirms the tonic key with repeated cadences. In Beethoven's later works, the coda grows to match the length and weight of the development, becoming a "second development" that provides further resolution.

The key scheme is the backbone:

| Section | Theme 1 key | Theme 2 key |
|:---|:---:|:---:|
| Exposition | tonic | dominant (or relative major) |
| Development | various, unstable | various, unstable |
| Recapitulation | tonic | tonic |

Sonata form is, at its core, an algorithm about keys. Given a tonic and a secondary key area, it generates a three-phase structure in which the secondary key is introduced, challenged, and resolved back into the tonic. The thematic content provides the material. The key scheme provides the logic.[^63]

## XI.F. Theme and Variations

In theme-and-variations form, a theme is stated, then transformed through a series of variations. The theme is typically simple: a clearly articulated melody with a transparent harmonic structure, often 8 or 16 measures in a simple binary or period form. Complexity is not the point. Clarity is. The theme must be memorable enough that the listener can track its persistence through the transformations to come.

Each variation preserves some structural essence of the theme while changing other parameters. The common techniques:

**Rhythmic variation** changes the durations while preserving the pitches (or their contour). A theme in quarter notes might be restated in eighth-note patterns, or in dotted rhythms, or in triplets. The melody is recognizable because the pitch sequence is intact, but the rhythmic feel is transformed.

**Harmonic variation** (reharmonization) replaces the original chords with different chords that support the same melody. A melody that sat over I, IV, V, I might be restated over I, ii, V7/V, V, I, enriching the harmonic palette. The melody remains. The harmonic ground beneath it shifts.

**Modal variation** changes the mode: major to minor, or the reverse. A theme in (0, major) restated in (0, minor) keeps the same tonic but replaces PCs 4, 9, and 11 with PCs 3, 8, and 10 (assuming natural minor). The contour of the melody is preserved. The color changes dramatically.

**Ornamental variation** (also called diminution) embellishes the melody with added notes: passing tones, neighbor tones, trills, turns. The original melody is still present as a skeleton, but it is clothed in faster-moving decorative figures.

**Textural variation** changes the arrangement of voices. A theme presented as a single melody with chordal accompaniment might reappear as a two-voice canon, or as a polyphonic texture with the melody in the bass, or as a virtuosic solo without accompaniment.

**Worked Example 87.** A theme in (5, major), 8 measures, with the progression I, V, I, IV, I, V7, I. Variation 1: same melody and harmony, but every quarter note is replaced by two eighth notes (rhythmic variation). Variation 2: same melody, but the harmony changes to I, iii, vi, IV, I, ii, V7, I (harmonic variation). Variation 3: the theme is restated in (5, minor), with PCs 9 and 2 replaced by PCs 8 and 1 in the melody and chords (modal variation). Variation 4: the melody is moved to the bass voice while a new counter-melody plays above it (textural variation). Each variation is recognizably "the same piece," yet each sounds different. The identity that persists through transformation is the theme's structural skeleton: its phrase lengths, its cadence points, its melodic contour.

The connection to transposition (Part IX) is instructive. Transposition changes pitch level but preserves all interval relationships. Variation changes other parameters (rhythm, harmony, mode, texture) but preserves some structural essence. Both operations are transformations that hold something fixed while altering something else. The ear tracks the fixed element and perceives the altered element as "variation on" the original, rather than as a completely new piece.

## XI.G. The 12-Bar Blues

The 12-bar blues is a fixed harmonic form: 12 measures with a prescribed chord progression that has served as the foundation of an extraordinary range of music for over a century. Blues, jazz, rhythm and blues, rock and roll, funk, and their descendants all draw from this template.

The standard form, in Roman numerals:

| Measure | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Chord | I | I | I | I | IV | IV | I | I | V | IV | I | I (or V) |

The structure falls into three 4-measure phrases. Phrase 1 (measures 1 through 4): the tonic, establishing the key. Phrase 2 (measures 5 through 8): departure to the subdominant in measures 5 and 6, return to the tonic in measures 7 and 8. Phrase 3 (measures 9 through 12): the dominant in measure 9, subdominant in measure 10, tonic in measures 11 and 12. Measure 12 sometimes substitutes V for I as a **turnaround**, creating harmonic momentum back to the top of the form for the next chorus.

The three phrases mirror the lyric structure of traditional blues: a statement (phrase 1), the statement repeated (phrase 2, over different harmony), and a response (phrase 3). The harmonic scheme supports this AAB text pattern with a musical arc from stability (I), through departure (IV), to tension (V) and resolution (I).

**Worked Example 88.** Realize the 12-bar blues in the key of (0, major). The three chords: I = {0, 4, 7}, IV = {5, 9, 0}, V = {7, 11, 2}. The progression: {0, 4, 7} for four measures, {5, 9, 0} for two, {0, 4, 7} for two, {7, 11, 2} for one, {5, 9, 0} for one, {0, 4, 7} for two. Total: 12 measures. Each chord is a major triad. The entire form uses only three chords, all diatonic to the key, cycling through the functional pattern T, S, T, D, S, T.

In practice, the blues uses **dominant seventh chords on every degree**: I7 = {0, 4, 7, 10}, IV7 = {5, 9, 0, 3}, V7 = {7, 11, 2, 5}. This is harmonically remarkable. In diatonic major-key theory, only V naturally takes a dominant seventh (the chord built on scale degree 5 with diatonic thirds stacked: 7, 11, 2, 5). The I chord "should" have a major seventh: Imaj7 = {0, 4, 7, 11}. The IV chord "should" have a major seventh: IVmaj7 = {5, 9, 0, 4}. By placing a minor seventh (10 semitones above the root) on I and IV, the blues violates diatonic harmony deliberately. Every chord has the dominant seventh's interval structure, the interval template {0, 4, 7, 10}, but none functions as a dominant in the classical sense. The I7 chord rests. The IV7 chord departs. The V7 chord resolves. Their shared interval structure gives the blues its distinctive harmonic color, where every chord carries a hint of tension that never fully resolves.[^64]

**Worked Example 89.** Realize the 12-bar blues with dominant sevenths in the key of (7, major). The major scale from 7: {7, 9, 11, 0, 2, 4, 6}. I7: root 7, template {0, 4, 7, 10} transposed by 7 = {7, 11, 2, 5}. IV7: root 0, transposed = {0, 4, 7, 10}. V7: root 2, transposed = {2, 6, 9, 0}. Verify: I7 = {7, 11, 2, 5} has intervals 4, 3, 3 from root. Dominant seventh structure. IV7 = {0, 4, 7, 10}: same intervals. V7 = {2, 6, 9, 0}: 2 to 6 = 4, 6 to 9 = 3, 9 to 0 = 3. Same structure. All three chords share the {0, 4, 7, 10} template, each at a different transposition level.

Several common variations on the standard form exist:

The **quick-change blues** substitutes IV for I in measure 2, giving a faster harmonic rhythm at the opening: I, IV, I, I, IV, IV, I, I, V, IV, I, V. The early move to IV adds momentum.

The **jazz blues** enriches the harmony with ii-V substitutions and chromatic passing chords. A typical jazz blues in (0, major):

| Measure | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Chord | I7 | IV7 | I7 | I7 | IV7 | IV7 | I7 | vi7 | ii7 | V7 | I7 | ii7-V7 |

Here, measures 8 through 10 introduce the ii-V-I turnaround (the circle progression from Part VIII), and the final measure uses a ii-V turnaround to cycle back to the top. More elaborate jazz blues versions introduce tritone substitutions (replacing V7 with a dominant seventh chord whose root is a tritone away), secondary dominants, and chromatic approach chords.

The **minor blues** transposes the form into a minor key, typically replacing I with i (minor triad or minor seventh), IV with iv, and keeping V as a dominant seventh (to preserve the leading-tone resolution). In (0, minor): i7 = {0, 3, 7, 10}, iv7 = {5, 8, 0, 3}, V7 = {7, 11, 2, 5}.[^65]

The 12-bar blues is, in a precise sense, an algorithm. Given a key (a tonic pitch class), it generates a complete 12-measure chord progression. The input is one number. The output is a fully specified harmonic structure. The algorithm admits variations (quick-change, jazz, minor), each of which modifies the template while preserving its essential proportions and functional arc. For over a hundred years, musicians have fed different keys, tempos, rhythmic feels, and melodic ideas into this algorithm and produced an inexhaustible variety of music from a form that fits in a single table.

> **Algorithm: Generate 12-Bar Blues**
>
> **Input:** a tonic pitch class t
>
> **Output:** a 12-measure chord progression
>
> **Step 1.** Compute I7 = {t, (t+4) mod 12, (t+7) mod 12, (t+10) mod 12}.
>
> **Step 2.** Compute IV7 = {(t+5) mod 12, (t+9) mod 12, t, (t+3) mod 12}.
>
> **Step 3.** Compute V7 = {(t+7) mod 12, (t+11) mod 12, (t+2) mod 12, (t+5) mod 12}.
>
> **Step 4.** Assign chords to measures: I7, I7, I7, I7, IV7, IV7, I7, I7, V7, IV7, I7, I7.

**Worked Example 90.** Apply the algorithm with t = 3. I7 = {3, 7, 10, 1}. IV7 = {8, 0, 3, 6}. V7 = {10, 2, 5, 8}. The 12-measure progression: {3, 7, 10, 1} four times, {8, 0, 3, 6} twice, {3, 7, 10, 1} twice, {10, 2, 5, 8} once, {8, 0, 3, 6} once, {3, 7, 10, 1} twice. A complete blues in the key of 3, generated mechanically from a single input.

# Part XII: TEXTURE, COUNTERPOINT, AND SET THEORY

The pitch-class system built in Parts I through XI treats music as a sequence of events in one voice: a melody, a chord progression, a scale. Real music is rarely so simple. Multiple voices sound at once, each with its own rhythm and contour. Instruments differ in color even when they play the same note. A performer shapes a phrase through volume, attack, and sustain, none of which appear in the pitch-class representation. This final Part addresses what the integers leave out, and then, in its closing sections, formalizes what the integers have been doing all along.

## XII.A. Dynamics and Articulation

A note in the system developed so far is a pitch class, a duration, and an octave. Play PC 4 for one quarter note in octave 4, and the note is fully specified, at least on paper. In performance, two more dimensions come into play: how loud the note is, and how it begins and ends.

Volume is a continuous parameter. Sound intensity is measured in decibels (dB), a logarithmic scale, and the range from the softest playable note to the loudest spans roughly 40 to 50 dB on most instruments. Traditional notation discretizes this continuum into a handful of markings. From softest to loudest: *pp* (pianissimo), *p* (piano), *mp* (mezzo-piano), *mf* (mezzo-forte), *f* (forte), *ff* (fortissimo). These are approximate zones, not precise values. A *forte* on a flute occupies a different decibel range than a *forte* on a trumpet. The markings are relative instructions: play louder, play softer, play at a moderate level.

Between these discrete levels, gradual changes are possible. A crescendo is a smooth increase in volume over a span of notes. A decrescendo (or diminuendo) is a smooth decrease. These are indicated by hairpin symbols in traditional notation, or by the words themselves written below the staff. The result is a continuous arc of intensity laid over the discrete sequence of pitches and rhythms.

Articulation governs the shape of individual notes. Four common articulations cover most of the territory:

**Staccato** means short and detached. The note sounds for less than its full written duration, with silence filling the gap before the next note. A staccato quarter note might ring for only an eighth note's worth of time, followed by an eighth note of silence. The effect is crisp, pointillistic.

**Legato** means smooth and connected. Each note flows into the next with no audible gap. On a wind instrument, this means sustaining the air stream across note changes. On a piano, it means holding each key until the next is depressed. The effect is singing, continuous.

**Accent** means a stronger attack on the note's onset. The note begins louder than its surroundings, then settles to the prevailing dynamic level. An accented note punches through the texture.

**Tenuto** means the note is held for its complete written duration, with a slight emphasis. It is the opposite of staccato: where staccato truncates, tenuto insists on fullness.

These parameters are independent of pitch and rhythm. The note (4, 0) lasting one quarter note can be played *pp* staccato or *ff* legato. The pitch class, the octave, and the duration are identical in both cases. What changes is the expressive shape of the sound. Dynamics and articulation are performance parameters. They do not interact with the algebraic structure of pitch classes, intervals, or scales in any direct way. A transposition preserves all intervals regardless of whether the notes are played loudly or softly. An inversion maps pitch classes the same way whether the articulation is staccato or legato.

This independence is precisely why the integer system can defer these parameters without losing explanatory power. The mathematical structure of music theory lives in the pitch-class domain. Dynamics and articulation live in the performance domain. Both are essential to music. They simply operate on different axes.[^66]

## XII.B. Timbre and Tone Color

Two instruments can play the same note, the same pitch class in the same octave at the same volume, and sound completely different. A flute playing PC 0 in octave 4 does not sound like an oboe playing PC 0 in octave 4. The pitch is identical. The loudness can be matched. What differs is the quality of the sound, its color, its character. This quality is called timbre.

The physics behind timbre connects back to Part I. A vibrating string or air column does not produce a single frequency. It produces a fundamental frequency *f* (the frequency that determines the pitch class) along with a series of higher frequencies called overtones or harmonics. These overtones occur at integer multiples of the fundamental: 2*f*, 3*f*, 4*f*, 5*f*, 6*f*, and so on, extending upward in principle without limit.

This is the harmonic series, and it deserves a careful look through the lens of pitch classes. Suppose the fundamental is PC *p* at some octave. The overtones, expressed in pitch-class terms, form a revealing sequence:

- *f* (the fundamental): PC *p*
- 2*f* (first overtone): one octave above the fundamental, so PC *p* again. Octave equivalence.
- 3*f* (second overtone): an octave plus a perfect fifth above the fundamental. Its pitch class is approximately (*p* + 7) mod 12.[^67]
- 4*f* (third overtone): two octaves above. PC *p* again.
- 5*f* (fourth overtone): two octaves plus a major third. Approximately (*p* + 4) mod 12.
- 6*f* (fifth overtone): two octaves plus a perfect fifth. Approximately (*p* + 7) mod 12.
- 7*f* (sixth overtone): falls between standard pitch classes, roughly two octaves plus a minor seventh. Approximately (*p* + 10) mod 12, though the fit is poor.

The word "approximately" matters. The overtone series produces frequencies in exact integer ratios, while equal temperament divides the octave into twelve equal logarithmic steps. The two systems do not align perfectly. The third harmonic (3*f*) produces a pure perfect fifth with frequency ratio 3:2, which is 701.96 cents. The equal-tempered perfect fifth is 700 cents. The difference, about 2 cents, is nearly inaudible. The fifth harmonic (5*f*) produces a pure major third at 386.31 cents, while the equal-tempered major third is 400 cents. That 14-cent discrepancy is audible to trained ears. This is the same tension between just intonation and equal temperament that Part I identified. The overtone series is nature's tuning. Equal temperament is the compromise that allows free transposition.[^68]

The crucial observation is that the intervals which sound most consonant, the perfect fifth (interval class 5, or 7 semitones) and the major third (interval class 4, or 4 semitones), are the intervals that appear earliest and most prominently in the overtone series. This is not a coincidence. When two notes form a perfect fifth, their overtone series overlap extensively. The third harmonic of the lower note matches the second harmonic of the upper note (both produce the same frequency). This overlap produces a sensation of blend, of fitting together. Consonance, at root, is overtone alignment.[^69]

Dissonance, by contrast, arises when overtone series clash. Two notes a semitone apart (interval class 1) have overtones that fall close together but not on top of each other, producing rapid interference patterns called beating. The ear perceives this as roughness, tension, instability. The consonance ranking established in Part II, where the perfect fifth and octave sit at the top and the semitone and tritone sit at the bottom, is a direct reflection of overtone alignment.

Different instruments emphasize different overtones, and this is what distinguishes their timbres. A clarinet's cylindrical bore reinforces primarily the odd-numbered harmonics: *f*, 3*f*, 5*f*, 7*f*. The even harmonics (2*f*, 4*f*, 6*f*) are suppressed. This gives the clarinet its hollow, woody quality. A flute, by contrast, produces a nearly pure tone, with the fundamental dominating and overtones falling off rapidly. Its sound is clear, simple, close to a sine wave. A violin, with its complex bowing action, produces a rich spectrum with strong energy across many harmonics, both odd and even. The brightness and warmth of a violin's tone come from this harmonic richness.

The overtone series thus closes a circle that began in Part I. The physical phenomenon of vibrating objects produces frequencies in integer ratios. The ear perceives certain combinations as consonant because their overtone series align. Equal temperament approximates those ratios closely enough that the consonance is preserved, while gaining the freedom of transposition. And the reason different instruments sound different on the same note is that each instrument weights the shared overtone series differently. Pitch class tells you which fundamental is sounding. Timbre tells you what the harmonic portrait of that fundamental looks like.[^70]

## XII.C. Texture

When music involves more than one voice or part, the relationship between those parts defines the texture. Texture is not about what notes are played. It is about how the parts relate to each other, whether they move together, independently, or in some combination.

**Monophony** is the simplest texture: a single melodic line with no accompaniment, no harmony, no second voice. One part, one pitch at a time. Gregorian chant in its original form is monophonic. A solo flute playing an unaccompanied melody is monophonic. The pitch-class analysis of Parts I through IX, which typically examines one melodic line or one chord at a time, implicitly assumes monophonic or homophonic texture.

**Homophony** places one voice in the foreground carrying the melody, while other voices provide harmonic support. The supporting voices move in rhythm with the melody, forming chords beneath it. Most popular music, most hymns, and most accompanied song falls into this category. The chord progressions of Part VIII assume homophonic texture: a melody over a sequence of chords, with the chords providing harmonic context and the melody providing the main line of interest. In homophony, the accompanying voices have no independent melodic identity. They serve the harmony.

**Polyphony** gives each voice independent melodic integrity. Two, three, four, or more lines sound simultaneously, each with its own contour, rhythm, and direction. The voices are peers, not leader and accompaniment. A fugue is the paradigmatic example: a subject (a short melody) enters in one voice, then another voice enters with the same subject while the first voice continues with new material, and so on until all voices are active, each pursuing its own path while fitting together vertically. The music of J. S. Bach represents the high point of polyphonic writing in the Western tradition.[^71]

**Heterophony** is less common in Western art music but appears in many folk traditions. Multiple voices or instruments perform the same melody simultaneously, but with different embellishments, ornaments, or slight timing variations. The result is a thickened, shimmering version of a single line, similar enough to be recognizable as one melody, different enough to create a rich texture.

These categories are not rigid. A piece can shift between textures. A string quartet might open with a single unaccompanied melody (monophony), add a chordal accompaniment in the lower strings (homophony), then break into four independent lines (polyphony), all within a few measures. Texture is a dimension of musical design, as much a compositional choice as key, tempo, or form.

Polyphony introduces a problem that monophony and homophony avoid. When multiple independent melodies sound simultaneously, their vertical combinations, the chords they happen to form at each beat, must be controlled. A melody that sounds beautiful on its own may, when combined with another melody, produce jarring dissonances or awkward parallels at certain points. The art of managing these vertical relationships while maintaining horizontal independence is counterpoint.

## XII.D. Counterpoint Basics

Counterpoint is the discipline of combining melodies. The word comes from the Latin *punctus contra punctum*, "point against point," meaning note against note. Its goal is to produce music that works in two dimensions simultaneously: each voice, considered alone, traces a satisfying melodic line (the horizontal dimension), and the notes sounding together at each moment form acceptable harmonic combinations (the vertical dimension).

The systematic study of counterpoint goes back centuries. Johann Joseph Fux codified the method in his 1725 treatise *Gradus ad Parnassum*, organizing the subject into five "species" of increasing rhythmic complexity. Generations of composers studied Fux's method, including Haydn, Mozart, and Beethoven. The species approach remains the standard pedagogical framework.

**First species: note against note.** Two voices move in whole notes (or whatever the base rhythmic unit is). At each beat, both voices sound a note, and the interval between them must be consonant. The consonant intervals, in pitch-class terms, are: unison (0 semitones), minor third (3), major third (4), perfect fifth (7), minor sixth (8), major sixth (9), and octave (0, in a different register). Dissonant intervals, meaning the minor second (1), major second (2), perfect fourth (5), tritone (6), minor seventh (10), and major seventh (11), are forbidden between the two voices at any beat.

The perfect fourth (5 semitones) deserves a note. In two-voice counterpoint, it is treated as dissonant, even though it is the inversion of the consonant perfect fifth. The reason is acoustic: when only two voices sound, a fourth above the bass creates an ambiguity about which note is the root, producing instability. In three or more voices, the fourth can appear above voices other than the bass without this problem. The classification of the fourth shifts depending on context, a reminder that consonance is not purely a property of interval class but also of voicing.

Beyond the consonance requirement, first species imposes several constraints on how the voices move:

**No parallel fifths or octaves.** If voice 1 and voice 2 form a perfect fifth (7 semitones apart), the next beat cannot also be a perfect fifth reached by both voices moving in the same direction. The same prohibition applies to parallel octaves (both voices moving to an interval of 0 in a higher or lower register). The reason is perceptual: parallel fifths and octaves cause the two voices to fuse into what sounds like a single, thickened line, destroying the independence that counterpoint aims to maintain. Two voices moving in parallel fifths stop sounding like two voices. They sound like one voice with a shadow.

**No voice crossing.** The upper voice must remain above the lower voice at all times. If the soprano dips below the alto, or the alto below the tenor, the listener loses track of which line is which. Each voice must stay in its own register to remain perceptually distinct.

**Contrary motion preferred.** When one voice moves up, the other should move down. This is not an absolute rule, but a strong preference. Contrary motion maximizes the independence of the voices: they are going in opposite directions, so neither one sounds like an echo or shadow of the other. Parallel motion (both voices moving the same direction by different intervals) is acceptable but less interesting. Similar motion (both moving the same direction, arriving at a consonance) is allowed with care. Oblique motion (one voice stays on the same note while the other moves) is always safe.

**Approach to the cadence.** The final interval should be a perfect octave or a unison, and at least one voice should arrive there by step (moving 1 or 2 semitones). Approaching the final note by a large leap weakens the sense of resolution. The ideal cadence has both voices converging by step from opposite directions: the upper voice moving down by a semitone or whole step, the lower voice moving up.

These rules, taken together, define a constraint-satisfaction problem. Given a fixed melody called the *cantus firmus* (a pre-existing melody, usually simple and stepwise), the task is to compose a second melody, the counterpoint, such that every vertical interval is consonant and every transition between beats satisfies the motion constraints.

**Worked Example 91.** A cantus firmus in the lower voice consists of the pitch classes [0, 2, 4, 5, 7, 5, 4, 2, 0]. Find a first-species counterpoint in the upper voice. At each beat, the upper voice must form a consonant interval (3, 4, 7, 8, 9, or 12 semitones above) with the lower voice, and successive intervals must avoid parallel fifths and octaves.

One valid solution: [7, 9, 11, 0, 4, 0, 11, 9, 7]. Checking intervals above the cantus: 7-0 = 7 (P5), 9-2 = 7 (P5)... parallel fifths on beats 1 and 2. Rejected. Try again: [7, 9, 0, 0, 4, 0, 0, 9, 7]. Intervals: 7 (P5), 7 (P5) again. Still parallel. The cantus rises by step (0 to 2), so if the upper voice also rises and maintains a fifth, parallels result.

Better solution: [7, 11, 0, 0, 4, 0, 11, 11, 7]. Intervals: 7 (P5), 9 (M6), 8 (m6), 7 (P5), 9 (M6), 7 (P5), 7 (P5), 9 (M6), 7 (P5). Check for parallels: beats 1 to 2 move from P5 to M6 (voices diverge, fine). Beats 3 to 4: m6 to P5, contrary motion, fine. Beats 5 to 6: M6 to P5. Lower voice moves 7 to 5 (down 2), upper voice moves 4 to 0 (down 4). Same direction, arriving at P5. This is "direct fifth," approached by similar motion with both voices moving in the same direction. In strict counterpoint, this is discouraged when the upper voice moves by leap. Upper voice 4 to 0 is a leap of 4 semitones, so this is problematic.

The exercise illustrates why counterpoint is hard. The constraints interact. Satisfying the consonance requirement at each individual beat is straightforward. Satisfying all the motion constraints simultaneously, across every pair of consecutive beats, requires careful planning. The algorithm is essentially backtracking search: choose a note for the upper voice at beat 1, check all constraints, proceed to beat 2, check again, and if a constraint is violated, backtrack and try a different note. For a nine-note cantus firmus with roughly six valid consonant choices at each beat, the search space is large, but the constraints prune it aggressively.

**Second species** doubles the rhythmic density: two notes in the counterpoint against each note in the cantus firmus. The first note of each pair falls on a strong beat and must be consonant, following all the first-species rules. The second note falls on a weak beat and may be dissonant, provided it functions as a passing tone, a note that connects two consonances by step. If the strong beat has the upper voice at PC 7 and the next strong beat requires PC 9, the weak beat can be PC 8 (a dissonant interval against the cantus, but reached and left by step). The dissonance is fleeting, occurring on the unstressed part of the beat, and the stepwise motion gives it a sense of direction. The listener hears it not as a harsh clash but as a note in transit.

**Third species** quadruples the density: four notes against one. The principles extend naturally. Strong-beat consonance remains mandatory. Weak-beat dissonances are allowed as passing tones and neighbor tones (a note that steps away from a consonance and immediately returns). Fourth species introduces suspensions: a consonant note is held (suspended) across the bar line, becoming dissonant against the new cantus note on the strong beat, and then resolving downward by step to a consonance. The suspension creates a controlled dissonance on the strong beat itself, a calculated tension followed by release. Fifth species combines all the previous rhythmic textures freely.

The extension to three and four voices adds further considerations. With three voices, every pair of voices must satisfy the two-voice rules, and every beat should produce a reasonably complete chord. Incomplete chords (missing the third, or doubling the root excessively) sound thin. Spacing between voices matters: wide gaps between adjacent voices can create a hollow texture, while voices too close together may muddy each other's independence.

Counterpoint is to harmony what syntax is to vocabulary. Harmony names the chords and classifies their functions (Part VIII). Counterpoint governs how voices move between those chords, which notes can sound together, and how dissonance is prepared and resolved. A Roman numeral analysis (Part VIII) tells you that the progression is I to V. Counterpoint tells you how each voice gets from its note in the I chord to its note in the V chord, and what happens along the way.

## XII.E. Pitch Class Set Theory

The final section of this manuscript formalizes the framework that has been operating beneath the surface since Part I. Pitch classes, intervals, transposition, inversion: all of these have appeared as tools applied to specific problems. Pitch class set theory unifies them into a single algebraic system and reveals structure that the individual tools, used piecemeal, cannot show.

A **pitch-class set** (PCS) is any subset of Z₁₂. A single note is a PCS with one element: {0}. A dyad is a PCS with two: {0, 7}. A triad is a PCS with three: {0, 4, 7}. A scale is a PCS with seven (or five, or six, or eight, depending on the scale). The chromatic scale is the PCS containing all twelve elements: {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11}, which is Z₁₂ itself. The empty set is also a PCS, though not a musically interesting one.

Every chord, scale, and melodic fragment discussed in this manuscript is a PCS. The major triad {0, 4, 7}, the natural minor scale {0, 2, 3, 5, 7, 8, 10}, the whole-tone scale {0, 2, 4, 6, 8, 10}: all are subsets of Z₁₂, differing only in cardinality and membership.

**Operations on pitch-class sets.** Two operations have appeared throughout the manuscript. Now they can be stated in full generality.

**Transposition.** For any integer *n* and any PCS *S*:

T_n(S) = {(p + n) mod 12 : p in S}

Every element of the set is shifted by the same amount. Part IX defined this operation and showed that it preserves all intervals within the set. A major triad transposed by T_5 is still a major triad. A melodic fragment transposed by T_7 has the same contour and the same interval sequence. Transposition changes the absolute pitch classes but preserves the internal structure.

**Inversion.** For any PCS *S*:

I(S) = {(12 - p) mod 12 : p in S}

Equivalently, I(p) = (-p) mod 12. Each pitch class is reflected across the axis at PC 0. If you visualize the twelve pitch classes on a clock face, inversion is a mirror reflection through the 0-6 axis: PC 1 maps to PC 11, PC 2 maps to PC 10, PC 3 maps to PC 9, and so on. PC 0 and PC 6 are fixed points.

**Transposed inversion.** Combining these two operations yields T_nI:

T_nI(S) = {(n - p) mod 12 : p in S}

First invert, then transpose by *n*. This operation is more flexible than plain inversion because it allows the axis of reflection to be placed anywhere, not just at PC 0. T_0I is the same as I. T_1I reflects across a different axis. The 12 transpositions and 12 transposed inversions together form a group of 24 operations, called the T/I group, which acts on the set of all PCSs.[^72]

**Worked Example 92.** Apply T_3I to the major triad {0, 4, 7}. For each element: (3 - 0) mod 12 = 3, (3 - 4) mod 12 = 11, (3 - 7) mod 12 = 8. The result is {3, 11, 8}, which sorted is {3, 8, 11}. Check: internal intervals are 8-3 = 5, 11-8 = 3, 11-3 = 8. Compare to the minor triad template {0, 3, 7}: intervals are 3, 4, 7. The set {3, 8, 11} transposed to start at 0: subtract 3 from each element, giving {0, 5, 8}. The intervals 5 and 3 do not match {0, 3, 7} directly. Rewrite: {0, 5, 8} has intervals 5, 3, 4. Starting from 8: {8, 11, 3}, intervals 3, 4, 5. Starting from 11: {11, 3, 8}, intervals 4, 5, 3. The most compact ordering is {8, 11, 3} with intervals 3, 4, 5 and span (3 - 8) mod 12 = 7. This is a minor triad rooted on PC 8.

**Normal form.** A PCS can be written in many orderings. The set {0, 7, 4} and the set {4, 7, 0} and the set {7, 0, 4} are all the same PCS, just listed in different orders. Normal form selects a canonical ordering by choosing the rotation that produces the most compact arrangement.

The algorithm: list the elements of the PCS in ascending order around the clock. Consider every rotation (every possible starting element). For each rotation, compute the span from first element to last element (measured clockwise, mod 12). Choose the rotation with the smallest span. If two rotations tie on span, break the tie by comparing the first internal interval, then the second, choosing the rotation with the smaller intervals packed toward the beginning.

**Worked Example 93.** Find the normal form of {0, 4, 7}. Elements in ascending order: 0, 4, 7. Three rotations:

- Starting at 0: [0, 4, 7]. Span = (7 - 0) = 7.
- Starting at 4: [4, 7, 0]. Span = (0 - 4) mod 12 = 8.
- Starting at 7: [7, 0, 4]. Span = (4 - 7) mod 12 = 9.

Smallest span is 7, achieved by [0, 4, 7]. Normal form: [0, 4, 7].

**Worked Example 94.** Find the normal form of {0, 5, 8}. Elements in ascending order: 0, 5, 8. Three rotations:

- Starting at 0: [0, 5, 8]. Span = 8.
- Starting at 5: [5, 8, 0]. Span = (0 - 5) mod 12 = 7.
- Starting at 8: [8, 0, 5]. Span = (5 - 8) mod 12 = 9.

Smallest span is 7, achieved by [5, 8, 0]. Normal form: [5, 8, 0].

**Prime form.** Normal form depends on the specific pitch classes in the set. To compare sets that might be transpositions or inversions of each other, a further reduction is needed. Prime form strips away both transposition and inversion to produce a canonical representative of the entire *set class*: the family of all PCSs related by T_n and T_nI operations.

The algorithm: (1) Find the normal form of the PCS. Transpose it so the first element is 0. Call this candidate A. (2) Invert the PCS, find the normal form of the inversion, and transpose so the first element is 0. Call this candidate B. (3) Compare A and B by reading their intervals left to right. Choose whichever is more compact (smaller intervals packed toward the left). That is the prime form.

**Worked Example 95.** Find the prime form of the major triad {0, 4, 7}.

Step 1: Normal form is [0, 4, 7] (from Worked Example 85). Already starts at 0. Candidate A = [0, 4, 7].

Step 2: Invert. I({0, 4, 7}) = {0, 8, 5}. Sort: {0, 5, 8}. Find normal form (from Worked Example 86): [5, 8, 0]. Transpose to start at 0: subtract 5 from each element. (8 - 5) = 3, (0 - 5) mod 12 = 7. Candidate B = [0, 3, 7].

Step 3: Compare A = [0, 4, 7] and B = [0, 3, 7]. First elements both 0. Second element: A has 4, B has 3. B is smaller. Prime form = [0, 3, 7].

**Worked Example 96.** Find the prime form of the minor triad {0, 3, 7}.

Step 1: Normal form. Three rotations of {0, 3, 7}: [0, 3, 7] span 7, [3, 7, 0] span 9, [7, 0, 3] span 8. Best: [0, 3, 7], span 7. Already starts at 0. Candidate A = [0, 3, 7].

Step 2: Invert. I({0, 3, 7}) = {0, 9, 5}. Sort: {0, 5, 9}. Normal form: [0, 5, 9] span 9, [5, 9, 0] span 7, [9, 0, 5] span 8. Best: [5, 9, 0], span 7. Transpose to 0: [0, 4, 7]. Candidate B = [0, 4, 7].

Step 3: Compare A = [0, 3, 7] and B = [0, 4, 7]. Second element: A has 3, B has 4. A is smaller. Prime form = [0, 3, 7].

The major triad and the minor triad have the same prime form: [0, 3, 7]. They belong to the same set class. This is the deepest statement the integer system can make about the relationship between major and minor. They are not opposites. They are not merely related by sharing two out of three interval classes. They are, in the language of set theory, the same object viewed from two directions. The major triad is the minor triad reflected. The minor triad is the major triad reflected. Inversion maps one to the other, and since set-class membership ignores the distinction between a set and its inversion, they collapse into a single equivalence class.[^73]

This equivalence was invisible in the letter-name system. C major (C, E, G) and C minor (C, E♭, G) look like different chords with one note altered. A minor (A, C, E) and C major (C, E, G) have no obvious visual similarity on a staff. In the integer system, the relationship is exposed: {0, 4, 7} and {0, 3, 7} are inversionally equivalent, members of the same set class [0, 3, 7]. The integers make the hidden symmetry visible.

**Interval vector revisited.** Part II introduced the interval vector as a way to catalog the intervals present in a PCS. The interval vector counts, for each interval class from 1 to 6, how many pairs of elements in the set exhibit that interval class. For the major triad {0, 4, 7}: the pairs are (0,4) with IC 4, (0,7) with IC 5, and (4,7) with IC 3. The interval vector is [0, 0, 1, 1, 1, 0].[^74]

**Worked Example 97.** Compute the interval vector of the minor triad {0, 3, 7}. The pairs: (0,3) has IC 3, (0,7) has IC 5, (3,7) has IC 4. The interval vector is [0, 0, 1, 1, 1, 0]. Identical to the major triad.

This is not a coincidence. It is a theorem: two PCSs in the same set class always have the same interval vector. Transposition preserves all intervals (shown in Part IX). Inversion maps interval class *k* to interval class *k* (since inverting both notes of a pair does not change the distance between them, only the direction, and interval class ignores direction). Therefore, any operation in the T/I group preserves the interval vector. Sets in the same class must share the same vector.

The converse, however, is false. Two PCSs can have the same interval vector and belong to different set classes. These are called **Z-related sets**. The name comes from the German *Zygotisch* (twinned). The simplest example involves two tetrachords (4-element PCSs): {0, 1, 4, 6} and {0, 1, 3, 7}. Both have the interval vector [1, 1, 1, 1, 1, 1], containing exactly one of each interval class, a remarkably even distribution. Yet no transposition or inversion maps one to the other. They are distinct set classes with identical interval fingerprints.[^75]

**Worked Example 98.** Verify that {0, 1, 4, 6} and {0, 1, 3, 7} are Z-related. First, compute interval vectors.

For {0, 1, 4, 6}: pairs and ICs: (0,1)=1, (0,4)=4, (0,6)=6, (1,4)=3, (1,6)=5, (4,6)=2. Vector: [1, 1, 1, 1, 1, 1].

For {0, 1, 3, 7}: pairs and ICs: (0,1)=1, (0,3)=3, (0,7)=5, (1,3)=2, (1,7)=6, (3,7)=4. Vector: [1, 1, 1, 1, 1, 1].

Same vector. Now check if they are related by T_n or T_nI. The prime form of {0, 1, 4, 6}: normal form candidates are [0, 1, 4, 6] (span 6), [1, 4, 6, 0] (span 11), [4, 6, 0, 1] (span 9), [6, 0, 1, 4] (span 10). Best: [0, 1, 4, 6]. Candidate A = [0, 1, 4, 6]. Invert: I({0, 1, 4, 6}) = {0, 11, 8, 6} = {0, 6, 8, 11}. Normal form: [6, 8, 11, 0] (span 6), [8, 11, 0, 6] (span 10), [11, 0, 6, 8] (span 9), [0, 6, 8, 11] (span 11). Best: [6, 8, 11, 0]. Transpose to 0: [0, 2, 5, 6]. Candidate B = [0, 2, 5, 6]. Compare A = [0, 1, 4, 6] and B = [0, 2, 5, 6]. Second element: 1 < 2. Prime form = [0, 1, 4, 6].

The prime form of {0, 1, 3, 7}: normal form candidates are [0, 1, 3, 7] (span 7), [1, 3, 7, 0] (span 11), [3, 7, 0, 1] (span 10), [7, 0, 1, 3] (span 8). Best: [0, 1, 3, 7]. Candidate A = [0, 1, 3, 7]. Invert: I({0, 1, 3, 7}) = {0, 11, 9, 5} = {0, 5, 9, 11}. Normal form: [5, 9, 11, 0] (span 7), [9, 11, 0, 5] (span 8), [11, 0, 5, 9] (span 10), [0, 5, 9, 11] (span 11). Best: [5, 9, 11, 0]. Transpose to 0: [0, 4, 6, 7]. Candidate B = [0, 4, 6, 7]. Compare A = [0, 1, 3, 7] and B = [0, 4, 6, 7]. Second element: 1 < 4. Prime form = [0, 1, 3, 7].

Prime forms [0, 1, 4, 6] and [0, 1, 3, 7] are different. These sets are in distinct set classes. They are Z-related: same interval vector, different prime form.

Z-related sets are rare among small cardinalities but become more common among sets of 4, 5, and 6 elements. They represent a genuine limitation of the interval vector as a classifier. Two sets can contain the same intervals in the same quantities and still be structurally distinct. The interval vector captures the pairwise distances within a set but not their arrangement, their geometry on the clock face. Z-related sets prove that interval content alone does not determine set class.[^76]

**The full picture.** The total number of distinct PCSs of Z₁₂ is 2^12 = 4,096 (including the empty set). After grouping by transposition and inversion, these collapse into 352 set classes (considering both T_n and T_nI equivalence) or 224 T-classes (considering transposition alone). Allen Forte cataloged these set classes and assigned each a name in the form *n*-*m*, where *n* is the cardinality and *m* is an index number. The major and minor triads, prime form [0, 3, 7], are Forte number 3-11. The all-interval tetrachords of Worked Example 90 are 4-Z15 and 4-Z29, with the "Z" in Forte's naming indicating their Z-related status.[^77]

This apparatus, PCSs, transposition, inversion, normal form, prime form, interval vectors, set classes, provides a complete taxonomy of the harmonic and melodic materials available in the twelve-tone system. Every possible chord is classified. Every possible scale is classified. The relationships between them (which are transpositions of which, which are inversions of which, which share the same interval content) are all determined by the algebra of Z₁₂.

**Worked Example 99.** Classify the augmented triad {0, 4, 8}. Normal form: [0, 4, 8] (span 8), [4, 8, 0] (span 8), [8, 0, 4] (span 8). All rotations have the same span. Tie-breaking by first interval: [0, 4, 8] has first interval 4, [4, 8, 0] has first interval 4, [8, 0, 4] has first interval 4. All tied. Choose [0, 4, 8] by convention. Candidate A = [0, 4, 8]. Invert: I({0, 4, 8}) = {0, 8, 4} = {0, 4, 8}. The augmented triad is its own inversion. Candidate B = [0, 4, 8]. Prime form = [0, 4, 8]. This set is invariant under inversion, a consequence of its perfect symmetry: three equal intervals of 4 semitones dividing the octave into three equal parts. The augmented triad is Forte number 3-12.

**Worked Example 100.** Classify the diminished triad {0, 3, 6}. Normal form: [0, 3, 6] (span 6), [3, 6, 0] (span 9), [6, 0, 3] (span 9). Best: [0, 3, 6]. Candidate A = [0, 3, 6]. Invert: I({0, 3, 6}) = {0, 9, 6} = {0, 6, 9}. Normal form: [0, 6, 9] (span 9), [6, 9, 0] (span 6), [9, 0, 6] (span 9). Best: [6, 9, 0]. Transpose to 0: [0, 3, 6]. Candidate B = [0, 3, 6]. Prime form = [0, 3, 6]. The diminished triad is also self-inversional. Its Forte number is 3-10.

The integers 0 through 11 were chosen at the start of this manuscript to replace letter names with something more transparent. Pitch class set theory reveals how much was gained by that choice. The relationships between chords and scales that traditional theory describes in fragmented, case-by-case terms (relative keys, parallel keys, chord quality, mode) turn out to be instances of a small number of algebraic operations: transposition, inversion, and their combinations. Major and minor triads are not opposites. They are reflections of each other, members of the same set class, indistinguishable by interval content. Every scale, every chord, every melody is a subset of twelve integers, and the relationships between them are governed by the simplest arithmetic: addition and subtraction modulo 12.

The abstraction does not drain the music of its beauty. It reveals why the beauty was there all along. The perfect fifth sounds consonant because overtone series align. Major and minor triads share the same interval vector because inversion preserves pairwise distances. The circle of fifths organizes key relationships because 7 and 12 are coprime. These are not metaphors. They are facts, as verifiable as the frequency of a vibrating string, and they have been hiding in the integers since the first note sounded.

# Glossary

**Aeolian.** The sixth rotation of the diatonic scale step pattern, [2, 1, 2, 2, 1, 2, 2]. Identical to the natural minor scale. Section VI.B.

**Algorithm.** A step-by-step procedure that produces a determinate result from given inputs. Scales, chord constructions, and normal form computations are all algorithms in this manuscript. Section III.B and throughout.

**Augmented triad.** A three-note chord built from two stacked major thirds: template {0, 4, 8}. Divides the octave into three equal parts. Its interval vector is [0, 0, 0, 3, 0, 0]. Section VII.A.

**Beat.** The basic unit of rhythmic measurement. Beats group into measures according to the time signature. Section X.A.

**Binary form.** A two-part musical structure, typically labeled A-B. Each section may be repeated. Section XI.A.

**Blues scale.** A six-note scale with step pattern [3, 2, 1, 1, 3, 2] from root 0: {0, 3, 5, 6, 7, 10}. Contains the "blue notes" PC 3 and PC 6 (the minor third and tritone above the tonic). Section III.D.

**Cadence.** A harmonic formula that marks the end of a phrase. Common types include authentic (V to I), plagal (IV to I), half (ending on V), and deceptive (V to vi). Section VIII.C.

**Chord.** Three or more pitch classes sounding simultaneously. A subset of Z₁₂, typically of cardinality 3 or 4. Section VII.A.

**Chromatic scale.** The twelve-note scale containing all pitch classes: {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11}. Step pattern [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]. Section III.E.

**Circle of fifths.** The cyclic ordering of all 12 pitch classes generated by repeated addition of 7 (mod 12): 0, 7, 2, 9, 4, 11, 6, 1, 8, 3, 10, 5. Organizes key signatures, chord progressions, and modulatory distance. Section V.A.

**Compound interval.** An interval larger than an octave. Equivalent to a simple interval (within one octave) plus one or more octaves. A "ninth" is a second plus an octave. Section II.E.

**Compound meter.** A meter in which each beat subdivides into three equal parts. 6/8, 9/8, and 12/8 are compound meters. Section X.B.

**Consonance.** The perceptual quality of stability, rest, or blend between two or more simultaneous notes. Correlated with simple frequency ratios and overtone alignment. The most consonant intervals are the unison, octave, and perfect fifth. Section II.D.

**Counterpoint.** The art of combining two or more independent melodic lines so that their simultaneous combination produces acceptable harmonic intervals. Governed by rules of voice independence, consonance, and motion. Section XII.D.

**Diatonic.** Belonging to or derived from the seven-note major scale (or one of its modal rotations). The diatonic collection is any transposition of {0, 2, 4, 5, 7, 9, 11}. Section III.B.

**Diminished triad.** A three-note chord built from two stacked minor thirds: template {0, 3, 6}. Contains a tritone between root and fifth. Its interval vector is [0, 0, 2, 0, 0, 1]. Section VII.A.

**Dissonance.** The perceptual quality of tension, roughness, or instability between two or more simultaneous notes. Correlated with complex frequency ratios and overtone interference. Section II.D.

**Dominant.** The pitch class 7 semitones above the tonic. Also, the harmonic function associated with chords containing the leading tone (V, vii°), which create tension directed toward the tonic. Section IV.A and VIII.A.

**Dorian.** The second rotation of the diatonic scale step pattern: [2, 1, 2, 2, 2, 1, 2]. A minor-sounding mode with a raised sixth degree relative to natural minor. Section VI.B.

**Duration.** The length of time a note is held. Measured in beats or fractions of beats. Standard durations: whole note (4 beats), half note (2), quarter note (1), eighth note (1/2), sixteenth note (1/4). Section X.A.

**Enharmonic equivalence.** The principle that two different letter-name spellings can refer to the same pitch class. F# and G♭ are both PC 6. In the integer system, enharmonic equivalence is automatic: each pitch class has exactly one name. Section IV.C.

**Equal temperament.** The tuning system that divides the octave into twelve equal semitones, each with frequency ratio 2^(1/12). Enables free transposition at the cost of slightly impure intervals. Section I.C.

**Form.** The large-scale organization of a musical composition into sections, their relationships, and their ordering. Binary, ternary, rondo, and sonata are common forms. Section XI.A.

**Frequency.** The number of complete vibration cycles per second, measured in hertz (Hz). Determines the pitch of a note. Section I.A.

**Fundamental.** The lowest frequency produced by a vibrating body. Determines the perceived pitch class. Higher frequencies in the vibration (overtones) determine timbre. Section XII.B.

**Half-diminished.** A four-note chord with template {0, 3, 6, 10}. A diminished triad with a minor seventh added. Notated as ø7 or m7♭5. Built on the seventh degree of the major scale. Section VII.B.

**Harmonic minor.** A seven-note scale with step pattern [2, 1, 2, 2, 1, 3, 1]. Raises the seventh degree of the natural minor to create a leading tone. From root 0: {0, 2, 3, 5, 7, 8, 11}. Section III.C.

**Harmonic series.** The sequence of frequencies produced by a vibrating body: f, 2f, 3f, 4f, 5f, ... The ratios between these frequencies give rise to the natural intervals and explain consonance. Section XII.B.

**Hertz (Hz).** The unit of frequency. One hertz equals one vibration cycle per second. A440 (the standard tuning reference) vibrates at 440 Hz. Section I.A.

**Homophony.** A texture in which one voice carries the melody while other voices provide chordal accompaniment. The most common texture in Western popular and Classical-era music. Section XII.C.

**Interval.** The distance between two pitch classes, measured in semitones. Can be directed (upward or downward) or undirected (interval class). Section II.A.

**Interval class (IC).** The undirected distance between two pitch classes: min(d, 12-d), where d is the directed interval. Ranges from 0 to 6. Section II.A.

**Interval vector.** A six-element vector [n₁, n₂, n₃, n₄, n₅, n₆] counting the number of pairs in a PCS exhibiting each interval class from 1 to 6. Characterizes the interval content of a set. Section II.F.

**Inversion (interval).** An interval's complement with respect to the octave. The inversion of interval *d* is (12 - d) mod 12. A perfect fifth (7) inverts to a perfect fourth (5). Section II.C.

**Inversion (pitch class).** The operation I(p) = (12 - p) mod 12, reflecting a pitch class across the 0-6 axis of the Z₁₂ clock. Extended to sets: I(S) = {(12 - p) mod 12 : p in S}. Section XII.E.

**Ionian.** The first rotation of the diatonic scale step pattern: [2, 2, 1, 2, 2, 2, 1]. Identical to the major scale. Section VI.B.

**Key.** A pair (tonic, scale type) that establishes a pitch-class set and a hierarchy among its members. The key of (0, major) means tonic 0 with the major scale. Section IV.A.

**Key signature.** The set of pitch classes belonging to a key's scale. In traditional notation, indicated by sharps or flats at the beginning of a staff. Section IV.B.

**Leading tone.** The seventh degree of the major scale, 11 semitones above the tonic. Sits one semitone below the tonic and has a strong tendency to resolve upward. Section IV.A.

**Locrian.** The seventh rotation of the diatonic scale step pattern: [1, 2, 2, 1, 2, 2, 2]. The darkest diatonic mode. Rarely used as a tonal center because its tonic triad is diminished. Section VI.B.

**Lydian.** The fourth rotation of the diatonic scale step pattern: [2, 2, 2, 1, 2, 2, 1]. The brightest diatonic mode, with a raised fourth degree. Section VI.B.

**Major scale.** The seven-note scale with step pattern [2, 2, 1, 2, 2, 2, 1]. From root 0: {0, 2, 4, 5, 7, 9, 11}. The foundational scale of Western tonal music. Section III.B.

**Major triad.** A three-note chord with template {0, 4, 7}: a major third (4 semitones) plus a minor third (3 semitones), spanning a perfect fifth (7 semitones). Section VII.A.

**Melodic minor.** A seven-note scale with step pattern [2, 1, 2, 2, 2, 2, 1] (ascending form). Raises both the sixth and seventh degrees of the natural minor. From root 0: {0, 2, 3, 5, 7, 9, 11}. Section III.C.

**Meter.** The organizing pattern of strong and weak beats within a measure. Defined by the time signature. Section X.A.

**Minor scale.** Any of three related seven-note scales: natural minor [2, 1, 2, 2, 1, 2, 2], harmonic minor [2, 1, 2, 2, 1, 3, 1], and melodic minor [2, 1, 2, 2, 2, 2, 1]. Section III.C.

**Minor triad.** A three-note chord with template {0, 3, 7}: a minor third (3 semitones) plus a major third (4 semitones), spanning a perfect fifth (7 semitones). Inversionally equivalent to the major triad. Section VII.A.

**Mixolydian.** The fifth rotation of the diatonic scale step pattern: [2, 2, 1, 2, 2, 1, 2]. A major-sounding mode with a lowered seventh degree. Section VI.B.

**Mode.** A rotation of a cyclic step pattern. The seven diatonic modes are the seven rotations of [2, 2, 1, 2, 2, 2, 1]. Section VI.A.

**Modulation.** A change of key within a piece. The tonic shifts, reorienting the pitch-class hierarchy. Common techniques include pivot chord modulation and direct modulation. Section IX.D.

**Monophony.** A texture consisting of a single melodic line with no accompaniment. Section XII.C.

**Natural minor.** The seven-note scale with step pattern [2, 1, 2, 2, 1, 2, 2]. From root 0: {0, 2, 3, 5, 7, 8, 10}. Identical to the Aeolian mode. Section III.C.

**Normal form.** The rotation of a pitch-class set that produces the most compact arrangement (smallest span from first to last element). A canonical ordering for comparison. Section XII.E.

**Note number.** An integer uniquely identifying a note across all octaves: note number = 12o + p, where o is the octave and p is the pitch class. Also called MIDI number when offset by convention. Section I.F.

**Octave.** The interval of 12 semitones, corresponding to a frequency ratio of 2:1. Notes separated by an octave share the same pitch class. Section I.B.

**Octave equivalence.** The principle that notes differing by one or more octaves are treated as the same pitch class. PC 0 in octave 3 and PC 0 in octave 5 are both "the same note" in pitch-class terms. Section I.B.

**Overtone.** A frequency higher than the fundamental, produced by a vibrating body. The *n*th overtone has frequency (*n*+1)f, where *f* is the fundamental. The collection of overtones determines timbre. Section XII.B.

**Parallel keys.** Two keys sharing the same tonic but different scale types: (t, major) and (t, minor). They differ in 3 out of 7 pitch classes. Section IV.D.

**Pentatonic scale.** A five-note scale. The major pentatonic has step pattern [2, 2, 3, 2, 3]. From root 0: {0, 2, 4, 7, 9}. Section III.D.

**Period.** A melodic structure consisting of two phrases (antecedent and consequent), typically 4+4 measures, ending with a conclusive cadence. Section XI.B.

**Phrase.** A musical unit analogous to a sentence in prose. A coherent melodic idea with a beginning, middle, and end, typically 4 or 8 measures long. Section XI.B.

**Phrygian.** The third rotation of the diatonic scale step pattern: [1, 2, 2, 2, 1, 2, 2]. Characterized by a half-step above the root, giving it a dark, Spanish-inflected quality. Section VI.B.

**Pitch class (PC).** An integer from 0 to 11 representing a note's position within the octave, independent of which octave it occupies. PC 0 = C, PC 1 = C#/D♭, etc. The fundamental object of this manuscript. Section I.C.

**Pitch class set (PCS).** Any subset of Z₁₂. Chords, scales, and melodic fragments are all pitch-class sets. Section XII.E.

**Polyphony.** A texture of two or more independent melodic lines sounding simultaneously. Each voice has its own contour and rhythmic profile. Fugue is the paradigmatic example. Section XII.C.

**Polyrhythm.** The simultaneous use of two or more conflicting rhythmic patterns. Example: three beats against two (3:2). Section X.C.

**Prime form.** The canonical representative of a set class: the most compact version of a PCS after considering all transpositions and inversions. Used to determine whether two PCSs belong to the same set class. Section XII.E.

**Progression.** A sequence of chords unfolding in time. Described in Roman numerals for key-independence. Section VIII.B.

**Relative keys.** Two keys sharing the same pitch-class set but different tonics: (t, major) and ((t+9) mod 12, natural minor). Section IV.D.

**Rest.** A duration of silence. Rests mirror note durations: whole rest, half rest, quarter rest, etc. Section X.A.

**Rhythm.** The pattern of durations and accents in music. The temporal counterpart to pitch. Section X.A.

**Roman numeral analysis.** A system for labeling chords by their scale degree and quality within a key. Uppercase for major (I, IV, V), lowercase for minor (ii, iii, vi), lowercase with ° for diminished (vii°). Section VII.C.

**Rondo.** A musical form with a recurring main theme alternating with contrasting episodes: A-B-A-C-A or similar patterns. Section XI.A.

**Root.** The pitch class on which a chord is built. The root of the triad {0, 4, 7} is PC 0. The root determines the chord's letter name in traditional notation. Section VII.A.

**Scale.** An ordered subset of Z₁₂ defined by a step pattern (a sequence of intervals summing to 12). Section III.A.

**Scale degree.** A pitch class's position within a scale, numbered from 1 (the tonic) to 7 (for seven-note scales). Each degree carries functional tendencies within a key. Section IV.A.

**Secondary dominant.** A dominant-function chord (V or V7) temporarily tonicizing a scale degree other than the tonic. Notated V/x, where x is the target chord. Section VIII.D.

**Semitone.** The smallest standard interval in Western music: 1 pitch-class unit. The frequency ratio is 2^(1/12) in equal temperament. Section I.C.

**Sentence.** A melodic structure consisting of a basic idea, its repetition (possibly varied), and a continuation leading to a cadence. Typically 8 measures: 2+2+4. Section XI.B.

**Set class.** The equivalence class of all pitch-class sets related by transposition and/or inversion. Identified by its prime form. Section XII.E.

**Simple meter.** A meter in which each beat subdivides into two equal parts. 2/4, 3/4, and 4/4 are simple meters. Section X.B.

**Sonata form.** A large-scale musical structure consisting of exposition, development, and recapitulation. The most important form in Classical-era instrumental music. Section XI.A.

**Species counterpoint.** A pedagogical method for learning counterpoint through five progressive exercises (species), each adding rhythmic complexity. Codified by J. J. Fux in 1725. Section XII.D.

**Subdominant.** The pitch class 5 semitones above the tonic (the fourth scale degree). Also, the harmonic function associated with chords built on the fourth and second degrees (IV, ii). Section VIII.A.

**Syncopation.** Rhythmic emphasis on normally weak beats or weak parts of beats, creating a sense of displacement or surprise. Section X.C.

**Temperament.** A tuning system. Equal temperament divides the octave into 12 equal semitones. Other temperaments (just, meantone, Pythagorean) distribute the slight impurities of tuning differently. Section I.C.

**Tempo.** The speed at which beats occur, measured in beats per minute (BPM). Andante is roughly 76-108 BPM. Allegro is roughly 120-156 BPM. Section X.A.

**Tendency tone.** A scale degree with a strong pull toward a neighboring degree. The leading tone (degree 7) tends upward to the tonic. The fourth degree tends downward to the third. Section IV.A.

**Ternary form.** A three-part musical structure, A-B-A, where the first section returns after a contrasting middle section. Section XI.A.

**Texture.** The relationship between simultaneous voices or parts. Principal types: monophony, homophony, polyphony, heterophony. Section XII.C.

**Theme and variations.** A form in which a theme is stated and then repeated in altered versions (variations), each preserving some elements (harmony, melody, phrase structure) while changing others. Section XI.A.

**Timbre.** The quality of a sound that distinguishes one instrument from another playing the same pitch at the same volume. Determined by the relative strengths of overtones in the harmonic series. Section XII.B.

**Time signature.** A pair of numbers indicating the meter: the upper number gives beats per measure, the lower number gives the note value that receives one beat. 4/4 means four quarter-note beats per measure. Section X.A.

**Tonic.** The central pitch class of a key. The point of rest and resolution. All other pitch classes in the key are heard in relation to it. Section IV.A.

**Transposition.** The operation T_n(p) = (p + n) mod 12, shifting every pitch class in a set by the same amount. Preserves all intervals. Extended to sets: T_n(S) = {(p + n) mod 12 : p in S}. Section IX.A.

**Triad.** A three-note chord built from stacked thirds. The four triad types are major {0, 4, 7}, minor {0, 3, 7}, diminished {0, 3, 6}, and augmented {0, 4, 8}. Section VII.A.

**Tritone.** The interval of 6 semitones, exactly half the octave. The most dissonant interval. Its complement is itself: 12 - 6 = 6. Section II.D.

**Tuplet.** A rhythmic grouping that divides a beat into a number of equal parts different from the standard subdivision. A triplet divides a beat normally split in two into three equal parts. Section X.C.

**Two-component system.** The representation of any note as a pair (octave, pitch class), separating register from pitch-class identity. Section I.D.

**Voice leading.** The principles governing how individual voices (parts) move from one chord to the next. Smooth voice leading minimizes the distance each voice travels. Section VIII.B and XII.D.

**Whole-tone scale.** A six-note scale with step pattern [2, 2, 2, 2, 2, 2]. From root 0: {0, 2, 4, 6, 8, 10}. Divides the octave into six equal parts. Only two distinct transpositions exist. Section III.E.

**Z₁₂.** The set of integers modulo 12: {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11}. The algebraic structure underlying all pitch-class arithmetic in this manuscript. Addition, subtraction, and comparison are performed modulo 12. Section I.G.

# Bibliography

## Acoustics and Physics of Sound

Helmholtz, Hermann von. *On the Sensations of Tone as a Physiological Basis for the Theory of Music*. Translated by Alexander J. Ellis. London: Longmans, Green, and Co., 1885. Originally published in German, 1863. The foundational text linking the physics of vibration to musical perception. Helmholtz's analysis of overtones, combination tones, and consonance remains essential reading.

Rossing, Thomas D., F. Richard Moore, and Paul A. Wheeler. *The Science of Sound*. 3rd ed. San Francisco: Addison Wesley, 2002. A thorough introduction to acoustics, covering vibration, wave propagation, room acoustics, and the physics of musical instruments. Accessible to readers with a basic science background.

Benade, Arthur H. *Fundamentals of Musical Acoustics*. 2nd ed. New York: Dover, 1990. Originally published by Oxford University Press, 1976. A physicist's account of how instruments produce sound, with detailed treatment of resonance, impedance, and the behavior of air columns and strings.

## Standard Music Theory

Aldwell, Edward, Carl Schachter, and Allen Cadwallader. *Harmony and Voice Leading*. 5th ed. Boston: Cengage Learning, 2019. A comprehensive tonal harmony textbook emphasizing voice-leading principles and the connection between chord progressions and melodic motion. Widely used in university curricula.

Kostka, Stefan, Dorothy Payne, and Byron Alm en. *Tonal Harmony, with an Introduction to Post-Tonal Music*. 8th ed. New York: McGraw-Hill, 2018. Another standard university textbook, covering diatonic and chromatic harmony, form, and an introduction to twentieth-century techniques. Strong on worked examples and analytical exercises.

Laitz, Steven G. *The Complete Musician: An Integrated Approach to Theory, Analysis, and Listening*. 4th ed. New York: Oxford University Press, 2016. Integrates aural skills with written theory, progressing from basic diatonic harmony through chromaticism, form, and post-tonal analysis.

Piston, Walter. *Harmony*. 5th ed. Revised and expanded by Mark DeVoto. New York: W. W. Norton, 1987. A classic text, first published in 1941, known for its clarity and systematic approach to harmonic analysis. Piston's examples are drawn almost entirely from the common-practice repertoire.

## Counterpoint

Fux, Johann Joseph. *Gradus ad Parnassum*. Vienna, 1725. Translated by Alfred Mann as *The Study of Counterpoint*. New York: W. W. Norton, 1965. The treatise that codified species counterpoint. Written as a dialogue between a student and a master, it lays out the five species with rules and examples. Still in pedagogical use three centuries after publication.

Jeppesen, Knud. *Counterpoint: The Polyphonic Vocal Style of the Sixteenth Century*. Translated by Glen Haydon. New York: Dover, 1992. Originally published in Danish, 1931. A study of Palestrina-style counterpoint with rigorous attention to historical practice and voice-leading principles.

Salzer, Felix, and Carl Schachter. *Counterpoint in Composition: The Study of Voice Leading*. New York: Columbia University Press, 1989. Originally published by McGraw-Hill, 1969. Bridges species counterpoint and free composition, showing how contrapuntal principles operate in real music from Bach to Brahms.

## Mathematical Music Theory and Set Theory

Forte, Allen. *The Structure of Atonal Music*. New Haven: Yale University Press, 1973. The book that established pitch-class set theory as a formal analytical method. Forte's catalog of set classes, his system of set names, and his analysis of atonal works by Schoenberg, Webern, and Berg made this a landmark publication. Essential for understanding the apparatus of section XII.E.

Rahn, John. *Basic Atonal Theory*. New York: Longman, 1980. Reprinted by Schirmer Books. A concise, mathematically precise introduction to pitch-class set theory. Rahn's normal form algorithm differs slightly from Forte's in its tie-breaking procedure, a detail that can produce different normal forms for certain sets.

Straus, Joseph N. *Introduction to Post-Tonal Theory*. 4th ed. New York: W. W. Norton, 2016. The standard textbook for post-tonal analysis, covering pitch-class sets, twelve-tone serialism, and transformational theory. Clear exposition with many analytical examples from twentieth-century repertoire.

Morris, Robert. *Composition with Pitch-Classes: A Theory of Compositional Design*. New Haven: Yale University Press, 1987. An advanced treatment extending set theory into compositional practice, with attention to symmetry, combinatoriality, and the group-theoretic structure of pitch-class operations.

Lewin, David. *Generalized Musical Intervals and Transformations*. New Haven: Yale University Press, 1987. Reprinted by Oxford University Press, 2007. A profound reconceptualization of music theory in terms of transformations rather than objects. Lewin's GIS (Generalized Interval System) framework subsumes traditional interval theory and pitch-class set theory into a single abstract structure. Demanding but rewarding.

## History, Pedagogy, and General Reference

Lerdahl, Fred, and Ray Jackendoff. *A Generative Theory of Tonal Music*. Cambridge, MA: MIT Press, 1983. Applies ideas from generative linguistics to music, proposing formal rules for metric structure, grouping, and prolongational reduction. A rigorous attempt to model how listeners parse tonal music.

Temperley, David. *Music and Probability*. Cambridge, MA: MIT Press, 2007. Explores probabilistic and computational models of musical cognition, including key-finding algorithms, meter perception, and melodic expectation.

Tymoczko, Dmitri. *A Geometry of Music: Harmony and Counterpoint in the Extended Common Practice*. New York: Oxford University Press, 2011. Represents voice leadings as paths in geometric spaces, offering a visual and mathematical framework that unifies tonal and post-tonal harmony. Particularly strong on the geometry of chord spaces and the relationship between voice leading and harmony.

Clough, John, and Jack Douthett. "Maximally Even Sets." *Journal of Music Theory* 35, nos. 1-2 (1991): 93-173. Formalizes the notion of maximal evenness, showing that the diatonic scale and other important musical structures distribute their elements as evenly as possible around the chromatic circle. Directly relevant to the properties of the major scale explored in Part III.

Amiot, Emmanuel. *Music Through Fourier Space: Discrete Fourier Transform in Music Theory*. Cham: Springer, 2016. Applies the discrete Fourier transform to pitch-class sets, providing new measures of set properties (such as the degree of "majorness" or "chromaticness" of a set) and new perspectives on Z-related sets.

---

[^1]: The hertz (Hz) as a unit of frequency is named after Heinrich Hertz, who demonstrated electromagnetic waves in 1887. For a thorough treatment of frequency, vibration, and its relationship to pitch perception, see Thomas D. Rossing, F. Richard Moore, and Paul A. Wheeler, *The Science of Sound*, 3rd ed. (Addison-Wesley, 2002), chapters 1-4.

[^2]: The A440 tuning standard was adopted by the International Organization for Standardization as ISO 16 in 1975. The history of pitch standards is complex; before the twentieth century, concert pitch varied widely by region and era. See Hermann von Helmholtz, *On the Sensations of Tone*, trans. Alexander J. Ellis, 2nd English ed. (1885; repr., Dover, 1954), appendix XX, where Ellis documents historical pitch levels.

[^3]: The logarithmic nature of pitch perception was described mathematically by Gustav Fechner in the nineteenth century as part of his psychophysical law relating stimulus intensity to perceived magnitude. For a modern treatment of pitch perception as ratio-based, see Juan G. Roederer, *The Physics and Psychophysics of Music*, 4th ed. (Springer, 2008), chapter 2.

[^4]: The harmonic series and its role in consonance was first systematically described by Helmholtz in *On the Sensations of Tone* (1863/1954), Part I, chapters 2-4. Helmholtz demonstrated that the quality of consonance correlates with the alignment of overtone spectra between two tones. See also Roederer, *The Physics and Psychophysics of Music*, chapter 4, for a contemporary synthesis.

[^5]: The perceptual equivalence of octave-related pitches is one of the most robust findings in auditory psychology and appears cross-culturally. See Diana Deutsch, "The Paradox of Pitch Circularity," *Music Perception* 3, no. 3 (1986): 275-280, and Roederer, *The Physics and Psychophysics of Music*, 4th ed. (Springer, 2008), 29-31.

[^6]: The formalization of octave equivalence as a mathematical equivalence relation, and the resulting partition of frequencies into pitch classes, is standard in mathematical music theory. See David Benson, *Music: A Mathematical Offering* (Cambridge University Press, 2007), chapter 5; and Guerino Mazzola, *The Topos of Music* (Birkhauser, 2002), chapter 6.

[^7]: The historical question of why twelve divisions is addressed by, among others, Stuart Isacoff, *Temperament: How Music Became a Battleground for the Great Minds of Western Civilization* (Vintage, 2003), which traces the cultural and mathematical debates surrounding tuning systems. Gerald Balzano, "The Group-Theoretic Description of 12-Fold and Microtonal Pitch Systems," *Computer Music Journal* 4, no. 4 (1980): 66-84, offers a group-theoretic explanation for the musical utility of 12.

[^8]: The consolidation of twelve-tone equal temperament in Western music occurred gradually during the seventeenth and eighteenth centuries. J. Murray Barbour, *Tuning and Temperament: A Historical Survey* (Michigan State College Press, 1951; repr., Dover, 2004) provides the most comprehensive historical account. See also Isacoff, *Temperament*, chapters 8-12.

[^9]: The twelfth root of 2 as the equal-temperament semitone ratio was described mathematically as early as the sixteenth century by the Chinese scholar Zhu Zaiyu (1584) and independently by Simon Stevin in Europe (c. 1585). See Barbour, *Tuning and Temperament*, chapter 7; and Benson, *Music: A Mathematical Offering*, section 5.3.

[^10]: The convention of assigning 0 to C (and hence aligning the integer system with the letter-name system at C major) is standard in pitch-class set theory. See Allen Forte, *The Structure of Atonal Music* (Yale University Press, 1973), 1-3, and Joseph N. Straus, *Introduction to Post-Tonal Theory*, 4th ed. (W. W. Norton, 2016), chapter 1.

[^11]: This octave numbering convention, in which middle C is designated C4, was adopted by the Acoustical Society of America in 1939. See Robert W. Young, "Terminology for Logarithmic Frequency Units," *Journal of the Acoustical Society of America* 11, no. 1 (1939): 134-139.

[^12]: The frequency of C0 (approximately 16.35 Hz) falls below the commonly cited lower limit of human hearing, around 20 Hz, though individual thresholds vary. See Rossing, Moore, and Wheeler, *The Science of Sound*, 3rd ed., chapter 6, for a discussion of auditory thresholds.

[^13]: The MIDI specification assigns middle C the note number 60. See the MIDI 1.0 Detailed Specification, published by the MIDI Manufacturers Association (1983, updated 1996). The discrepancy with music-theory octave numbering arises because MIDI octave numbering begins at -1, so MIDI C4 = 60 = 12 * 5 + 0.

[^14]: The integers modulo 12 form a cyclic group under addition, denoted Z/12Z or simply Z_12. This is a standard result in abstract algebra. See, e.g., Joseph A. Gallian, *Contemporary Abstract Algebra*, 10th ed. (Cengage, 2021), chapter 4. For its application to music, see Benson, *Music: A Mathematical Offering*, chapter 11.

[^15]: Equal-temperament frequency tables are tabulated in numerous references. A convenient source is Rossing, Moore, and Wheeler, *The Science of Sound*, appendix A. The values here are computed from f = 440 * 2^((n-69)/12), where n is the MIDI note number, which is equivalent to the formula given in the text.

[^16]: Microtonal music systems do subdivide the semitone further (quarter-tones, sixth-tones, etc.), and some non-Western traditions use intervals smaller than a semitone. However, the twelve-tone equal-temperament semitone is the smallest standard interval in the Western system that this manuscript addresses. See Benson, *Music: A Mathematical Offering*, chapter 6, for a discussion of microtonal systems.

[^17]: The relationship between beating, roughness, and the perception of dissonance was first analyzed by Helmholtz in *On the Sensations of Tone*, Part II, chapter 10. The modern psychoacoustic model of roughness is elaborated in Ernst Terhardt, "Pitch, Consonance, and Harmony," *Journal of the Acoustical Society of America* 55, no. 6 (1974): 1061-1069; and in William A. Sethares, *Tuning, Timbre, Spectrum, Scale*, 2nd ed. (Springer, 2005), chapters 3-4.

[^18]: This relationship between a scale's internal symmetry and the number of its distinct transpositions is a consequence of the orbit-stabilizer theorem in group theory. If a scale S is invariant under a subgroup H of the transposition group Z_12, then the number of distinct transpositions of S equals [Z_12 : H] = 12 / |H|. See Benson, *Music: A Mathematical Offering*, section 11.4; and Mazzola, *The Topos of Music*, chapter 11.

[^19]: The pair (2, 11) should be verified: (11 - 2) mod 12 = 9, and (2 - 11) mod 12 = 3; IC = min(9, 3) = 3. So the pair (2, 11) contributes to IC 3. The four IC-3 pairs in the major scale are {0, 9}, {2, 5}, {2, 11}, and {4, 7}. See Straus, *Introduction to Post-Tonal Theory*, 4th ed., chapter 1, for interval vector computation methods.

[^20]: The property that the diatonic scale's interval vector contains all six interval classes is related to the concept of the diatonic set as a "deep scale." See Carlton Gamer, "Some Combinational Resources of Equal-Tempered Systems," *Journal of Music Theory* 11, no. 1 (1967): 32-59; and John Clough and Jack Douthett, "Maximally Even Sets," *Journal of Music Theory* 35, nos. 1-2 (1991): 93-173.

[^21]: The concept of tonal hierarchy, in which the tonic is the most stable pitch class and other degrees carry varying degrees of tension and tendency, has been empirically validated by Carol Krumhansl in *Cognitive Foundations of Musical Pitch* (Oxford University Press, 1990), especially chapters 2-4, using probe-tone experiments.

[^22]: This arithmetic pattern for key-signature accumulation follows directly from the structure of the circle of fifths. Each new sharp raises the fourth degree of the previous key by a semitone, and each new flat lowers the seventh degree. See Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed. (McGraw-Hill, 2018), chapter 4, for the standard presentation.

[^23]: Enharmonic equivalence of keys is a direct consequence of equal temperament. In unequal temperaments (meantone, well temperament), F-sharp major and G-flat major would differ in intonation, so they were treated as distinct keys. See Isacoff, *Temperament*, chapters 4-6, for the historical context.

[^24]: The derivation of the relative minor from the sixth degree of the major scale is covered in every standard theory textbook. See Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed. (Cengage, 2011), chapter 4; and Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 3.

[^25]: The fact that parallel major and minor keys differ in exactly three pitch classes can be verified by comparing the cumulative interval sums of [2, 2, 1, 2, 2, 2, 1] and [2, 1, 2, 2, 1, 2, 2] from any shared root. The result is a general property of these two step patterns. See Benson, *Music: A Mathematical Offering*, section 11.2.

[^26]: The theorem that an integer k generates Z_n if and only if gcd(k, n) = 1 is a standard result in number theory and group theory. See Gallian, *Contemporary Abstract Algebra*, 10th ed., theorem 4.3; and Benson, *Music: A Mathematical Offering*, chapter 11.

[^27]: For a formal treatment of generators and cyclic groups in the context of music, see Guerino Mazzola, *The Topos of Music* (Birkhauser, 2002), chapter 6; and Julian Hook, "Uniform Triadic Transformations," *Journal of Music Theory* 46, nos. 1-2 (2002): 57-126.

[^28]: The equivalence of the circle of fifths and the circle of fourths (traversed in opposite directions) follows from the fact that 5 + 7 = 12 ≡ 0 (mod 12), making 5 and 7 additive inverses in Z_12. See Benson, *Music: A Mathematical Offering*, section 11.3; and Straus, *Introduction to Post-Tonal Theory*, 4th ed., chapter 1.

[^29]: The use of the circle of fifths as a measure of key distance dates at least to the eighteenth century. For a modern formalization, see Carol Krumhansl, *Cognitive Foundations of Musical Pitch* (Oxford University Press, 1990), chapter 7, where perceptual key-distance judgments are shown to correlate strongly with circle-of-fifths distance.

[^30]: The count here is corrected in the text itself: (0, major) and (6, major) share PCs {5, 11}, so 2 PCs are shared and 5 differ. The broader point, that tritone-related keys are maximally distant, holds. See Krumhansl, *Cognitive Foundations of Musical Pitch*, chapter 7.

[^31]: The role of the circle of fifths in organizing chord progressions is a central topic in tonal harmony. The descending-fifth root motion pattern is discussed extensively in Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 7; and Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed., chapter 14.

[^32]: The medieval modal system inherited Greek names but reassigned them, sometimes inconsistently. The Dorian mode of medieval and modern theory does not correspond to the ancient Greek Dorian. See Harold S. Powers et al., "Mode," in *The New Grove Dictionary of Music and Musicians*, 2nd ed., edited by Stanley Sadie and John Tyrrell (Macmillan, 2001); and Thomas J. Mathiesen, *Apollo's Lyre: Greek Music and Music Theory in Antiquity and the Middle Ages* (University of Nebraska Press, 1999).

[^33]: The association of Phrygian mode with Spanish and flamenco music is well documented. The Phrygian cadence (a half cadence in which the bass descends by semitone to the dominant) is a hallmark of Baroque and flamenco style alike. See Peter Manuel, "Modal Harmony in Andalusian, Eastern European, and Turkish Syncretic Musics," *Yearbook for Traditional Music* 21 (1989): 70-94.

[^34]: The correspondence between the modal brightness ordering and the circle of fifths applied to scale degrees is discussed in Ian Ring, "A Study of Scales," available at ianring.com/musictheory/scales, and in Dmitri Tymoczko, *A Geometry of Music* (Oxford University Press, 2011), chapter 4. The connection is a structural consequence of the diatonic set being generated by consecutive fifths.

[^35]: Phrygian dominant (the fifth mode of harmonic minor) is widely used in flamenco, klezmer, and various Middle Eastern musical traditions. See Manuel, "Modal Harmony in Andalusian, Eastern European, and Turkish Syncretic Musics"; and Joshua Horowitz, "The Main Klezmer Modes," available at budowitz.com.

[^36]: The Lydian dominant scale and its use over altered dominant chords is a core concept in jazz theory. See Mark Levine, *The Jazz Theory Book* (Sher Music, 1995), chapters 4-5; and Jamey Aebersold, *Jazz Handbook* (Aebersold Jazz, 2010).

[^37]: Modal interchange (borrowing chords from parallel modes) is covered extensively in Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 21; and in Walter Everett, "Making Sense of Rock's Tonal Systems," *Music Theory Online* 10, no. 4 (2004).

[^38]: The distinction between a pitch-class set and a rooted chord (where one member is designated the root) is addressed in Straus, *Introduction to Post-Tonal Theory*, 4th ed., chapter 1. In tonal theory, the root is determined by the generative process of stacking thirds; in atonal theory, sets have no inherent root.

[^39]: The augmented triad's equal division of the octave into three parts is an instance of a maximally symmetric set. For the group-theoretic properties of equal-division sets, see Forte, *The Structure of Atonal Music*, 14-18; and Benson, *Music: A Mathematical Offering*, section 11.4.

[^40]: The fully diminished seventh chord's division of the octave into four equal parts (the four-fold symmetry) and its consequent enharmonic ambiguity is discussed in Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 17; and Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed., chapter 25.

[^41]: The treatment of the 6/4 chord (second inversion) as a special case requiring careful handling is a longstanding principle of common-practice harmony. See Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed., chapter 11; and Piston, *Harmony*, 5th ed. (Norton, 1987), chapter 16.

[^42]: The dominant 7#9 chord, often called the "Hendrix chord" or "Purple Haze chord," gained widespread recognition through Jimi Hendrix's use of it in "Purple Haze" (1967) and "Foxy Lady" (1967). The chord's simultaneous inclusion of both a major third and a minor third (enharmonically, the sharp ninth) gives it its distinctive biting quality. See Andy Aledort, "Deconstructing Hendrix," *Guitar World*, various issues; and Levine, *The Jazz Theory Book*, chapter 11.

[^43]: The term "suspended" refers to a practice originating in Renaissance counterpoint, where the fourth was literally "suspended" from a previous chord as a dissonance that resolved downward to the third. In modern usage, the sus chord is treated as a chord type in its own right, without necessarily resolving. See Piston, *Harmony*, 5th ed., chapter 11; and Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 13.

[^44]: The uniqueness of the dominant seventh chord on scale degree 5 as the only diatonic seventh chord containing a tritone between its third and seventh is discussed in Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed., chapters 12-14; and Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 7.

[^45]: The ubiquity of the I-V-vi-IV progression in popular music was famously satirized in the Axis of Awesome's comedy sketch "4 Chords" (2009), which demonstrated that dozens of hit songs share this harmonic pattern. For scholarly analysis, see Trevor de Clercq and David Temperley, "A Corpus Analysis of Rock Harmony," *Popular Music* 30, no. 1 (2011): 47-70.

[^46]: The plagal cadence's association with "Amen" at the end of hymns is a well-known convention in church music. For historical context, see Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed., chapter 13.

[^47]: The diatonic circle of fifths differs from the chromatic circle because one of the seven "fifths" between adjacent diatonic scale degrees is a diminished fifth (6 semitones) rather than a perfect fifth (7 semitones). This occurs between scale degrees 4 and 7 (or equivalently, 7 and 4 ascending). See Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 7; and Piston, *Harmony*, 5th ed., chapter 5.

[^48]: The smooth voice leading in ii-V-I progressions is a central topic in jazz theory and in Schenkerian analysis. For the jazz perspective, see Levine, *The Jazz Theory Book*, chapter 2. For voice-leading principles in classical harmony, see Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed., chapter 14.

[^49]: The chaining of secondary dominants through the circle of fifths is sometimes called a "chain of dominants" or "dominant prolongation." See Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 16; and Levine, *The Jazz Theory Book*, chapter 14.

[^50]: The minor iv chord borrowed into a major key is one of the most frequently cited examples of modal interchange. The progression I-IV-iv-I appears in songs ranging from Radiohead's "Creep" to numerous Broadway standards. See Walter Everett, "Making Sense of Rock's Tonal Systems," *Music Theory Online* 10, no. 4 (2004); and Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 21.

[^51]: The bVI-bVII-I progression (sometimes called the "Mario cadence" for its appearance in video game music) is a hallmark of film scoring and rock harmony. Its roots lie in modal mixture rather than functional harmony. See Nicole Biamonte, "Triadic Modal and Pentatonic Patterns in Rock Music," *Music Theory Spectrum* 32, no. 2 (2010): 95-110; and Everett, "Making Sense of Rock's Tonal Systems."

[^52]: Transposing instruments and their relationship to concert pitch are covered in Samuel Adler, *The Study of Orchestration*, 4th ed. (W. W. Norton, 2016), chapter 1. The transposition intervals for common instruments are standardized: B-flat trumpet sounds 2 semitones below written pitch, F horn sounds 7 semitones below, E-flat alto saxophone sounds 9 semitones below.

[^53]: Direct modulation (sometimes called "phrase modulation" or "truck driver's modulation" when it shifts up by a half or whole step) is a common device in popular music for heightening energy in final choruses. See de Clercq and Temperley, "A Corpus Analysis of Rock Harmony"; and Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 18.

[^54]: The modulatory potential of symmetrical chords (diminished seventh and augmented triad) is discussed in Aldwell, Schachter, and Cadwallader, *Harmony and Voice Leading*, 4th ed., chapters 25-26; and Kostka, Payne, and Almen, *Tonal Harmony*, 8th ed., chapter 18. Because the diminished seventh chord can be respelled enharmonically with any of its four notes as the root, it serves as a pivot to four different keys.

[^55]: The zero-pivot-chord result for tritone-related keys follows from the fact that they differ in the maximum number of pitch classes. The absence of common diatonic triads between keys six steps apart on the circle is verified here computationally. See Krumhansl, *Cognitive Foundations of Musical Pitch*, chapter 7, for perceptual evidence of key distance.

[^56]: The conception of a note as a pair of pitch and duration is formalized in various computational music models. See Guerino Mazzola, *The Topos of Music* (Birkhauser, 2002), chapter 6, for a mathematical treatment; and David Huron, *Sweet Anticipation: Music and the Psychology of Expectation* (MIT Press, 2006), chapters 10-11, for the perceptual dimensions.

[^57]: Rubato as expressive deviation from strict tempo has been studied empirically through performance analysis. See Bruno H. Repp, "Diversity and Commonality in Music Performance: An Analysis of Timing Microstructure in Schumann's 'Traumerei,'" *Journal of the Acoustical Society of America* 92 (1992): 2546-2568; and Eric Clarke, "Expression in Performance: Generativity, Perception, and Semiosis," in *The Practice of Performance*, ed. John Rink (Cambridge University Press, 1995).

[^58]: Dave Brubeck's "Take Five" (1959), composed by Paul Desmond, is in 5/4 time with a 3+2 grouping. It was one of the first jazz recordings in an irregular meter to achieve widespread commercial success. See Ted Gioia, *The History of Jazz*, 3rd ed. (Oxford University Press, 2021), for context on Brubeck's rhythmic innovations.

[^59]: Brian Ferneyhough and Elliott Carter are prominent composers associated with "New Complexity," a style that employs densely layered, nested tuplets and polyrhythmic structures. See Richard Toop, "Four Facets of 'The New Complexity,'" *Contact* 32 (1988): 4-50; and David Schiff, *The Music of Elliott Carter*, 2nd ed. (Cornell University Press, 1998).

[^60]: The structural parallel between harmonic dissonance (requiring a tonal context to function as dissonance) and rhythmic syncopation (requiring a metric context to function as displacement) is discussed in Fred Lerdahl and Ray Jackendoff, *A Generative Theory of Tonal Music* (MIT Press, 1983), chapters 2-4, where metric and tonal structures are treated as parallel hierarchical systems.

[^61]: The appearance of the least common multiple (lcm) in both pitch (the circle of fifths generating Z_12) and rhythm (polyrhythmic cycle lengths) is an instance of the broader mathematical parallels between pitch and time organization. See Benson, *Music: A Mathematical Offering*, chapters 7 and 11; and Godfried Toussaint, *The Geometry of Musical Rhythm* (CRC Press, 2013), chapter 19.

[^62]: For the use of binary form in Baroque dance suites, see Jane R. Stevens, "Binary Form," in *The New Harvard Dictionary of Music*, ed. Don Michael Randel (Harvard University Press, 1986); and Mark Evan Bonds, *A History of Music in Western Culture*, 5th ed. (Pearson, 2017), chapters 9-10.

[^63]: Sonata form's dependence on tonal opposition and resolution is the central thesis of Charles Rosen, *Sonata Forms*, rev. ed. (W. W. Norton, 1988); and James Hepokoski and Warren Darcy, *Elements of Sonata Theory: Norms, Types, and Deformations in the Late-Eighteenth-Century Sonata* (Oxford University Press, 2006).

[^64]: The use of dominant seventh chord voicing on all three primary chords (I, IV, V) in the blues is a defining characteristic that sets blues harmony apart from common-practice diatonic harmony. See Jeff Todd Titon, *Early Downhome Blues: A Musical and Cultural Analysis*, 2nd ed. (University of North Carolina Press, 1994); and David Evans, "Blues," in *The New Grove Dictionary of Music and Musicians*, 2nd ed.

[^65]: The minor blues form and its characteristic substitution of minor triads for major ones on the tonic and subdominant degrees is discussed in Levine, *The Jazz Theory Book*, chapter 16; and Jerry Coker, *Elements of the Jazz Language for the Developing Improvisor* (Alfred Music, 1991).

[^66]: The orthogonality of pitch structure and performance parameters (dynamics, articulation, timbre) is a foundational assumption of pitch-class set theory. Forte, *The Structure of Atonal Music*, 1-5, explicitly restricts the theory to pitch-class relations, treating other parameters as outside its scope.

[^67]: The pitch class of the third harmonic (3f) relative to the fundamental is derived from the pure-ratio relationship: 3f is a perfect fifth (ratio 3:2) above 2f, and 2f is one octave above f. In equal-temperament pitch-class terms, the perfect fifth maps to 7 semitones, so the pitch class is approximately (p + 7) mod 12. See Helmholtz, *On the Sensations of Tone*, Part I, chapter 4; and Rossing, Moore, and Wheeler, *The Science of Sound*, chapter 7.

[^68]: The discrepancy between just-intonation intervals (derived from the harmonic series) and equal-temperament intervals is quantified in cents: 1 cent = 1/100 of a semitone. The perfect fifth differs by approximately 2 cents; the major third by approximately 14 cents. See Barbour, *Tuning and Temperament*, appendix; and Benson, *Music: A Mathematical Offering*, sections 5.3-5.4.

[^69]: The explanation of consonance as overtone alignment was first proposed by Helmholtz in *On the Sensations of Tone*, Part II. Modern psychoacoustic refinements distinguish between "sensory consonance" (the smoothness of two simultaneous tones, governed by overtone alignment and roughness) and "musical consonance" (a culturally influenced judgment). See Roederer, *The Physics and Psychophysics of Music*, chapter 5; and Richard Parncutt, *Harmony: A Psychoacoustical Approach* (Springer, 1989).

[^70]: The relationship between timbre and the relative amplitudes of harmonics in the overtone series is covered in Rossing, Moore, and Wheeler, *The Science of Sound*, chapters 7-12, with detailed analyses of specific instrument families. See also Neville H. Fletcher and Thomas D. Rossing, *The Physics of Musical Instruments*, 2nd ed. (Springer, 1998).

[^71]: For the polyphonic tradition culminating in J. S. Bach, see Christoph Wolff, *Johann Sebastian Bach: The Learned Musician* (W. W. Norton, 2000); and David Yearsley, *Bach and the Meanings of Counterpoint* (Cambridge University Press, 2002). The fugue as a polyphonic genre is discussed in Alfred Mann, *The Study of Fugue* (W. W. Norton, 1965; repr., Dover, 1987).

[^72]: The T/I group of 24 operations on pitch-class sets is the dihedral group of order 24, isomorphic to the direct product Z_12 x Z_2. See Forte, *The Structure of Atonal Music*, chapter 1; Straus, *Introduction to Post-Tonal Theory*, 4th ed., chapter 2; and Robert Morris, *Composition with Pitch-Classes* (Yale University Press, 1987), chapter 3.

[^73]: The equivalence of major and minor triads under inversion, placing them in the same set class, is one of the striking results of pitch-class set theory. Not all theorists accept this equivalence as musically meaningful; some prefer T-equivalence alone (grouping only by transposition), which keeps major and minor triads in separate classes. See Straus, *Introduction to Post-Tonal Theory*, 4th ed., 48-52, for discussion.

[^74]: The interval vector was introduced by Howard Hanson in *Harmonic Materials of Modern Music* (Appleton-Century-Crofts, 1960) under the name "intervallic analysis." Allen Forte adopted and formalized the concept in *The Structure of Atonal Music* (Yale University Press, 1973), chapter 1. The notation and computation method used here follows Straus, *Introduction to Post-Tonal Theory*, 4th ed., chapter 1.

[^75]: Z-related sets were identified and cataloged by Forte in *The Structure of Atonal Music*, 21-24. The name "Z" comes from the German *Zygotisch* (twinned), indicating that two sets share the same interval vector without being related by transposition or inversion. See also Straus, *Introduction to Post-Tonal Theory*, 4th ed., 65-67.

[^76]: The existence of Z-related sets demonstrates a fundamental limitation of the interval vector: it is a necessary but not sufficient condition for set-class equivalence. The problem of characterizing exactly which sets are Z-related remains an active area of research. See Emmanuel Amiot, *Music Through Fourier Space* (Springer, 2016), chapter 5, for a Fourier-transform perspective on the Z-relation.

[^77]: Forte's catalog of set classes and his naming system (e.g., 3-11 for the major/minor triad, 4-Z15 for an all-interval tetrachord) are presented in Allen Forte, *The Structure of Atonal Music* (Yale University Press, 1973), appendix 1. The catalog lists all 220 set classes (under T/I equivalence) for cardinalities 0-12, with their prime forms, interval vectors, and Z-relations. Straus, *Introduction to Post-Tonal Theory*, 4th ed., appendix, provides an updated version of the catalog.
