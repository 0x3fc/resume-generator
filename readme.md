# Resume Generator

## Description

A expendable tool using Vue (webpack-simple) that generates resume with specific user data. User can make their own theme and add new resume block template by adding new CSS files (theme) and Vue files (template).

[Demo](http://resume.senhung.net)

## How To Use

1. Clone + Install

```bash
$ git clone https://github.com/senhungwong/resume-generator.git
```

```bash
$ cd resume-generator
```

```bash
$ npm install
```

2. Edit data

Copy `data.example.json` and name it `data.json`

Fill out the data in `data.json`

3. Testing

```bash
$ npm run dev
```

4. Deploying

```bash
$ npm run build
```

## Themes

### Make

Create your own theme using `src/themes/template.css`.

### Use

Use your own theme by changing `src/App.vue` 

```vue
<style>
@import './themes/<your-theme>.css';
</style>
```

## Template

### Make

Create your own template in `src/templates`

### Use

Import your own template to `src/App.vue`
