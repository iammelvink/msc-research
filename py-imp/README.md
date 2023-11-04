# msc-research-project-implementation

## Repository for my msc-research-project-implementation project

## This is the Python section

Written in **Python**

1. Methodologies/Project Management:

   - Agile

2. Coding Practices:

   - OOP (Object Oriented Programming)
   - MVC (Model View Controller)

3. Programming Languages/Frameworks:

   - R
   - Python
   - HTML (Not really a language)
   - CSS
   - JavaScript

## Live Demo (loading...)

- [dev](https://<>.amazonaws.com/dev 'dev')

## Instructions

1. Make sure you have these installed

   - [Mambaforge (faster Anaconda)]([https://www.x/download](https://github.com/conda-forge/miniforge/releases)/ 'Mambaforge (faster Anaconda)')
     - I used version 23.3.1-1 at time of creation

2. Clone this repository into your local machine using the terminal (mac) or
   [Gitbash (PC)](https://git-scm.com/download/win 'Gitbash (PC)')

   ```sh
   git clone https://github.com/iammelvink/msc-research-project-implementation.git
   ```

3. ```sh
   cd "py-imp"
   ```

4. Setup Mambaforge base env

   ```sh
   mamba env update --name base --file tools-for-base.yml && mamba activate base
   ```

5. Setup mamba project env:

   ```sh
   mamba env create --name project_n --file tools-tf.yml && mamba activate project_n
   ```

6. Setup "pip" project env:

   ```sh
   pip install -r requirements.txt
   ```

7. Add env to kernel:

   ```sh
   python -m ipykernel install --user --name project_n --display-name "Python 3.8 (project_n)"
   ```

8. Run JupyterLab

   ```sh
   jupyterlab
   ```

9. Open a `.ipynb` file in the `code` directory to get started

10. Enjoy!

## More Stuff

Check out some other stuff on
[Melvin K](https://github.com/iammelvink 'Melvin K GitHub page')
