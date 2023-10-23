# Are you receiving this?
A .wav file containing a recording of an unknown digital signal is provided.
Find a way to extract the flag from the digital data.

## Sigint
Difficulty: Medium

## Solution
- Identify the type of signal that has been recorded. Either by ear, or by searching through a database such as [sigidwiki](https://www.sigidwiki.com/wiki/Signal_Identification_Guide).

- Use a decoding software such as [PDW](https://www.discriminator.nl/pdw/index-en.html), decode the POCSAG packets into text.

- The flag WCS{P4g1ngDrSm1th} appears.

## Hint
Post Office Code Standardisation Advisory Group

## Explanation
Despite falling out of use by the general public, pagers are still extremely common. One of the most commonly misidentified signals in the world of wireless security is POCSAG, the most common protocol used by pager systems to communicate data to recipients. Pagers are commonly used in hospitals to alert doctors of patient needs, in industrial settings to alert plant operators of machine status, or to summon volunteer first responders such as firefighters and ambulance crews in the event of an emergency.