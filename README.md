gabrieljoelc/resume: ![CI](https://github.com/gabrieljoelc/resume/workflows/CI/badge.svg)

# Description

This is my personal resume in [FRESH](https://github.com/fresh-standard/FRESCA) format. I use [HackMyResume](https://github.com/hacksalot/HackMyResume) to generate output files from the YAML file(s). I use a forkk of [fresh-themes](https://github.com/gabrieljoelc/fresh-themes) for the styles.

# Build

Generate output using these commands:
```
# this line is an awkward hack because HackMyResume doesn't accept YAML for some reason
ruby -ryaml -rjson -e 'puts JSON.pretty_generate(YAML.load(ARGF))' < default.yml > default.json
# this is a fork that contains a custom theme
git clone git@github.com:gabrieljoelc/fresh-themes.git
# once my custom theme supports multiple formats (i.e. PDF, MS Word) I can specify index.all
npx hackmyresume BUILD default.json TO out/index.html -t fresh-themes/themes/jae
npx hackmyresume BUILD default.json TO out/default.pdf -t fresh-themes/themes/jae
open out/index.html
open out/default.pdf
```

# TODO
- [ ] Finish styling to the [spec](https://launchpad.animaapp.com/preview/rJjQRcK/gcresumemvp)
- [ ] Move theme to this repo and reduce to one build (factor out [fresh-themes](https://github.com/gabrieljoelc/fresh-themes))
- [ ] Support PDF output
- [ ] Update [LinkedIn](https://www.linkedin.com/in/gabrielchaney/) through build
- [ ] Update [Stack Overflow Developer Story](https://stackoverflow.com/users/story/34315) through build
- [ ] Update [Standard Resume](https://standardresume.co/gabrielchaney) through build
- [x] ~~Include Codeship status in site~~ Move build to GitHub Actions
- [x] Include this repo in site (see this [commit](https://github.com/gabrieljoelc/fresh-themes/commit/0f4c0f71e409f2a70b43d72881a1f4eebd9723fa))
- [ ] Open PR for [HackMyResume](https://github.com/hacksalot/HackMyResume) to accept YAML input instead of just JSON
