Add Custome Style Sheet
==============================================================================

- This is :red:`Red` text.
- This is :blue:`Blue` text.
- This is :green:`Green` text.

1. Add your custom ``.css`` file. it should sitting at ``./_static/css/xxx.css``, let's say ``custom-style.css``, in this Style Sheet, you should assign diffrent style by class name.
2. Tell sphinx to add this Style Sheet in ``conf.py``::

    def setup(app):
        app.add_stylesheet('css/custom-style.css')
3. Define the class name with a role in ``.custom-style.rst`` file (Name doesn't matter, but has to starts with ``.``. Then everytime you use ``:rolename:`Some Text`, you will give ``Some Text`` a pre-defined html tag class.
4. Include this role definition ``.rst`` file everywhere in ``conf.py``::

    rst_prolog = '\n.. include:: .custom-style.rst\n'

Done!