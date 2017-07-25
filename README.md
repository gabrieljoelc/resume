Codeship Status for gabrieljoelc/resume: [ ![Codeship Status for gabrieljoelc/resume](https://app.codeship.com/projects/bdde7d00-5339-0135-6a9a-3e11013d5227/status?branch=master)](https://app.codeship.com/projects/234886)

Codeship Status for gabrieljoelc/fresh-themes: [ ![Codeship Status for gabrieljoelc/fresh-themes](https://app.codeship.com/projects/acdce700-5346-0135-125a-62c2a1758ec6/status?branch=master)](https://app.codeship.com/projects/234906)

This is my personal resume in FRESH format. I use [HackMyResume](https://github.com/hacksalot/HackMyResume) to generate output files from the YAML file(s).

Generate output using these commands:
```
# this line is an awkward hack because HackMyResume doesn't accept YAML for some reason
ruby -ryaml -rjson -e 'puts JSON.pretty_generate(YAML.load(ARGF))' < default.yml > default.json
# this is a fork that contains a custom theme
git clone git@github.com:gabrieljoelc/fresh-themes.git
npm install hackmyresume -g
# once my custom theme supports multiple formats (i.e. PDF, MS Word) I can specify index.all
hackmyresume BUILD default.json TO out/index.html -t fresh-themes/themes/jae
open out/index.html
```
