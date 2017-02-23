# glyphicons2tikz
I wrote this tool because I wanted to use the bootstrap glyphicons in a paper of mine. It's quite simple to use. The output of this tool results in an svg file for each glyphicon- and tex-file for direct integration into latex.

# Installation
```bash
# install dependencies
sudo apt-get install git nodejs npm python -y
# install svg2tikz
git clone https://github.com/kjellmf/svg2tikz
cd svg2tikz
sudo python setup.py install
# install glyphicons2tikz
git clone https://github.com/chrisdecker1201/glyphicons2tikz
cd glyphicons2tikz
# copy configuration
cp config.json.sample config.json
npm install
npm start
```

# Usage
The default of the script gives you black icons, but you can change the color in the _config.json_ to every possible color. Use HTML standard, for example: #ff00ff.

To use the icons in latex add the following packages to your file.

```latex
\usepackage{tikz}
\usepackage{standalone}
```

I configured the output of the tool with the _tikz_\__output_-parameter into my latex project and now I can write a paragraph like this:
```latex
\includestandalone[height=9pt]{tikz/eye-open}I really love to use many icons in my text \includestandalone[height=9pt]{tikz/king}
```
