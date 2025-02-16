# ResuMeow
Welcome to Reslumeow! An automaic CV generator written in nu.

This brutal script allows you to create a beautifully formatted CV in LaTeX from a simple YAML input file and command-line parameters.

<h1 align="center">
  <img src="imgs/mascot.jpg" alt="Local Image">
</h1>
<h3 align="center">
  <a href="imgs/example_cv.pdf">View an example</a>
</h3>

## Usage

### Command Line

To generate a CV, use the following command:

```bash
nu template.nu --input <path_to_input_yaml> --img <path_to_image> --output <output_pdf_path> [--color <hex_color_code>] [--language <language>]
```

- `--input`: Path to the YAML file containing the CV data.
- `--img`: Path to the image file to be included in the CV.
- `--output`: Path where the generated PDF will be saved.
- `--color`: (Optional) Hex color code for the CV theme. Default is `304263`.
- `--language`: (Optional) language to use for the headers. Default is `eng`. Supported languages are:
  - eng
  - it
  - fr
  - es
  - de

### YAML Input File

The input YAML file should be structured as follows:

- `name`: The name of the individual.
- `profile`: A list of profile descriptions.
- `desiderata`: A list of job desires or requirements.
- `languages`: A list of languages known.
- `contacts`: Contact information including `mail`, `phone`, and `links`.
- `key_competences`: A list of key competences with `name` and `text`.
- `transversal_competences`: A list of transversal competences with `name` and `text`.
- `work_experiences`: A list of work experiences with `title`, `company`, `dates`, `description`, and optional `items`.
- `education`: A list of educational qualifications with `title`, `institution`, and `grade`.

You can find an example one [here](input.yaml)

## Limitations of the Graphics

- The template uses a fixed layout, which may not accommodate all content if the input data is too extensive.
  - The `Competences` section must fit in one page.
  - The `Experiences` section must fit in one page.
- The color scheme is limited to a single customizable color, which may not suit all branding needs.
- The image size and placement are fixed, which might not be ideal for all types of images.

Feel free to contribute!

