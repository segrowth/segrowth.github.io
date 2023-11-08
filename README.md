# Local Development Setup for Jekyll Blog

This guide will help you to set up a local development environment for our Jekyll blog post page using the [Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy/). 
The steps will ensure that you can build and run the site on your local machine, regardless of whether you're using macOS or Windows.

## Prerequisites

Before you start, make sure you have the following installed on your system:
- Ruby (version 2.5.0 or above)
- RubyGems
- GCC and Make
- npm (Node.js package manager)

### For macOS:

1. Install Homebrew (if not already installed):
   ```sh
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
   ```

2. Install Ruby:
   ```sh
   brew install ruby
   ```

3. Add the brew ruby path to your shell configuration:
   ```sh
   echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile
   ```

4. Reload your shell configuration:
   ```sh
   source ~/.bash_profile
   ```
5. Install npm by installing Node.js:
   ```sh
   brew install node
   ```

### For Windows:

1. Download and install Ruby+Devkit from [RubyInstaller for Windows](https://rubyinstaller.org/).

2. Follow the prompts and ensure that the 'Add Ruby executables to your PATH' option is checked.

3. Download and install Node.js (which includes npm) from the [official Node.js website](https://nodejs.org/).

## Installation

1. Install Jekyll and Bundler:
   ```sh
   gem install jekyll bundler
   ```

2. Clone the blog repository:
   ```sh
   git clone git@github.com:segrowth/segrowth.github.io.git
   cd segrowth.github.io
   ```

3. Install dependencies from the Gemfile:
   ```sh
   bundle install
   ```
4. Build assets
   ```sh
   npm i && npm run build
   ```

## Running the Blog Locally

1. Build the site:
   ```sh
   bundle exec jekyll build
   ```

2. Run server locally (Optional)
   ```sh
   bundle exec jekyll serve --watch
   ```

3. Run server locally including drafts (Optional)
   ```sh
   bundle exec jekyll serve --watch --drafts
   ```

4. Now browse to [http://localhost:4000](http://localhost:4000) to view the site.

## Troubleshooting

- If you encounter any issues with bundle installation, you may need to install the necessary dependencies manually or run `bundle update` before `bundle install`.

- On macOS, if you face permissions issues, you may need to use `sudo` for installing gems.

- On Windows, if Jekyll fails to run, make sure to check the execution policy permissions and that Ruby is correctly added to PATH.

## Additional Resources

- [Jekyll documentation](https://jekyllrb.com/docs/)
- [Chirpy theme documentation](https://github.com/cotes2020/jekyll-theme-chirpy/wiki)
