# Karol Duszczyk - Personal Portfolio

Personal portfolio website built with Jekyll, showcasing my projects and skills in IoT Engineering.

🌐 **Live Site:** [karoldus.github.io](https://karoldus.github.io)

## About

I'm an IoT Engineering student at Warsaw University of Technology. This site presents my technical projects, courses, and achievements.

## Tech Stack

- **Jekyll 4.3** - Static site generator
- **Bootstrap** - Responsive framework
- **GitHub Pages** - Hosting
- **Custom Collections** - Projects organized as Jekyll collection

## Project Structure

```
├── _config.yml          # Jekyll configuration
├── _projects/           # Project portfolio items
│   ├── bip.md          # Touchless button project
│   ├── daft.md         # Python course
│   ├── forbot.md       # Technical writing
│   └── pbl3.md         # IoT system
├── _layouts/            # Page templates
├── _includes/           # Reusable components
├── _data/               # Site data (navigation, etc.)
├── _sass/               # Styles (Bootstrap customization)
├── css/                 # Compiled CSS
├── img/                 # Images and assets
└── js/                  # JavaScript

```

## Local Development

### Prerequisites

- Ruby (3.0+)
- Bundler

### Setup

```bash
# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# Visit
http://localhost:4000
```

### Adding New Projects

Create a new file in `_projects/` with front matter:

```yaml
---
layout: inner
title: 'Project Name'
date: 2025-01-01          # Actual completion date
order: 5                   # Display order (lower = first)
time_range: '01.2025 - 02.2025'
categories: project
tags: [Python, IoT, Arduino]
featured_image: 'img/posts/project-name.png'
project_link: 'https://github.com/username/repo'
button_icon: 'github'
button_text: 'View Project'
lead_text: 'Brief project description'
---

Detailed project description here...
```

## Configuration

Key settings in `_config.yml`:

- **Site title and description** - Update in `_data/global.yml`
- **Navigation** - Configure in `_data/nav.yml`
- **Projects collection** - Configured for custom project display
- **Plugins** - jekyll-paginate for project organization

## Deployment

Automatically deployed via GitHub Pages on push to main branch.

## Theme

Based on [Phantom theme](https://github.com/jamigibbs/phantom) by Jami Gibbs, heavily customized for project portfolio use.

## License

See [LICENSE](LICENSE) file.

## Contact

- **GitHub:** [@karoldus](https://github.com/karoldus)
- **LinkedIn:** [duszczykkarol](https://linkedin.com/in/duszczykkarol)

---

© 2025 Karol Duszczyk

Place the modal window template in any place you'd like the user to click for the contact form.
The template will display a link to click for the contact form modal window:

```
{% include contact.html %}
{% include contact-modal.html %}
```

**Animation Effects**

Animations with CSS classes are baked into the theme. To animate a section or element, simply add the animation classes:

```
<div id="about-me" class="wow fadeIn">
  I'm the coolest!
</div>
```

For a complete list of animations, see the [animation list](http://daneden.github.io/animate.css/).

**Pagination**

By default, pagination on the home page will activate after 10 posts. You can change this within `_config.yml`. You can add the pagination to other layouts with:

```
  {% for post in paginator.posts %}
    {% include post-content.html %}
  {% endfor %}

  {% include pagination.html %}
```

Read more about the [pagination plugin](http://jekyllrb.com/docs/pagination/).

### Credit

* Bootstrap, http://getbootstrap.com/, (C) 2011 - 2016 Twitter, Inc., [MIT](https://github.com/twbs/bootstrap/blob/master/LICENSE)

* Wow, https://github.com/matthieua/WOW, (C) 2014 - 2016 Matthieu Aussaguel
, [GPL](https://github.com/matthieua/WOW#open-source-license)

* Animate.css, https://github.com/daneden/animate.css, (C) 2016 Daniel Eden, [MIT](https://github.com/daneden/animate.css/blob/master/LICENSE)
