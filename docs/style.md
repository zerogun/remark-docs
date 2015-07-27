#3. Customize Styles

##3.1 Using CSS
All style changes, fixes, and improvements made for Remark will typically be added to ```assets/css``` folder.
The customize styles for 3rd plugins are in each plugin folders under ```assets/lib/``` folder.

To prevent losing your changes, you should add all of your customizations to a new stylesheet and include it separately in your pages. **Note** Also you must disable all ```grunt-less``` tasks in ```Gruntfile.js```.

##3.2 Using LESS
 [Bootstrap](http://getbootstrap.com/) is use [Less](http://lesscss.org/) as CSS pre-processor system. It will give you access to all the tools to perform even the most complex customizations with ease. So it is highly recommended that you switch to use the [Less](http://lesscss.org/) system as it is far superior, and offers a great deal of features and optimizations.

All the original [Less](http://lesscss.org/) files used for development are included for you to modify.

    src/less/
    ├── bootstrap/ (basic bootstrap less styles)
    ├── bootstrap_extend/ (improvements styles for remark)
    ├── mixins/ (basic less mixins from bootstrap)
    ├── mixins_extend/ (more useful mixins we defined)
    ├── components/
    ├── examples/
    ├── fonts/
    ├── sections/
    ├── widgets/
    └── layouts/

We also contain the 3rd plugins less files in ```src/vendor``` folder.

If you're new to [Less](http://lesscss.org/) and want to give it a try, you can find all the information you need here: **[http://lesscss.org/](http://lesscss.org/)**

##3.3 Easily Customize
This section is only for [Less](http://lesscss.org/) users.

We have added many features that allow variables, mixins, functions and many other techniques that allow you to make CSS more maintainable, themable and extendable. You will find them in ```src/less/mixins_extend``` and you can use them to write the styles you like.

In fact there is a simpler way to customize Remark. We have defined many variables in remark.
If you want a customized site, you just change them and use ```grunt css``` command to compile **css**. The style will be changed.

The core variables is defined in:

* **src/less/vars_bootstrap.less**: bootstrap override variables
* **src/less/vars_site.less**: site variables
* **src/less/vars_color.less**: color variables

More variables is defined on the header of each **less** files. For example:

    /* src/less/bootstrap_extend/alerts.less */
    @alert-padding-horizontal:        20px;

    @alert-list-padding-left:         13px;
    @alert-list-item-padding-left:    7px;