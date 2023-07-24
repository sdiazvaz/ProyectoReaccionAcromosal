# Pelican on GitLab Pages

Example [Pelican] website using GitLab Pages. Check the resulting website here: <https://pages.gitlab.io/pelican>

Learn more about [GitLab Pages](https://about.gitlab.com/stages-devops-lifecycle/pages/) and the [official
documentation](https://docs.gitlab.com/ce/user/project/pages/), including
[how to fork a project like this one to get started](https://docs.gitlab.com/ee/user/project/pages/getting_started_part_two.html#fork-a-project-to-get-started-from).

---

## GitLab CI

This project's static Pages are built by [GitLab CI][ci], following the steps
defined in the file [`.gitlab-ci.yml`](.gitlab-ci.yml).

## Building locally

To work locally with this project, you'll have to follow the steps below:

1. Fork, clone or download this project
1. [Install][] Pelican
1. Regenerate and serve on port 8000: `make devserver`
1. Add content

Read more at Pelican's [documentation].

## GitLab User or Group Pages

To use this project as your user/group website, you will need to perform
some additional steps:

1. Rename your project to `namespace.gitlab.io`, where `namespace` is
your `username` or `groupname`. This can be done by navigating to your
project's **Settings > General (Advanced)**.

2. Adjust Pelican's `SITEURL` configuration setting in `publishconf.py` to
the new URL (e.g. `https://namespace.gitlab.io`)

Read more about [GitLab Pages for projects and user/group websites][pagesdoc].

## Use a custom theme

To use a custom theme:

1. Visit <https://github.com/getpelican/pelican-themes> and pick the name of
   the theme you want to use.
1. Uncomment the following lines from `.gitlab-ci.yml`, replacing `<theme_name>`
   with the name of the theme you chose:

   ```yaml
   - svn export https://github.com/getpelican/pelican-themes/trunk/<theme-name> /tmp/<theme-name>
   - pelican-themes --install /tmp/<theme-name>
   ```

1. Edit `pelicanconf.py` and add the theme:

   ```plaintext
   THEME = '/tmp/<theme-name>'
   ```

For more information, see the discussion in [issue #1](https://gitlab.com/pages/pelican/-/issues/1).

## Did you fork this project?

If you forked this project for your own use, please go to your project's
**Settings** and remove the forking relationship, which won't be necessary
unless you want to contribute back to the upstream project.

## Troubleshooting

1. CSS is missing! That means two things:

    Either that you have wrongly set up the CSS URL in your templates, or
    your static generator has a configuration option that needs to be explicitly
    set in order to serve static assets under a relative URL.

[ci]: https://about.gitlab.com/gitlab-ci/
[pelican]: http://blog.getpelican.com/
[install]: https://docs.getpelican.com/en/stable/install.html
[documentation]: http://docs.getpelican.com/
[pagesdoc]: https://docs.gitlab.com/ce/user/project/pages/getting_started_part_one.html
