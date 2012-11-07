# Theme Loader

#### Version 1.3.0 (2012-11-06)

---

### Table Of Contents

1. [About the Project](#about-the-project)
2. [How to User](#how-to-use)
3. [Methods](#methods)
4. [License](#license)

---

### About the Project

Theme Loader is a CodeIgniter library that allows developer to easily determine the file path and URL of theme directories. With so many different ways to define a URL path with multiple environment bootstraps, it's critical that a library handle this to make things easy and consistent.

### Asynchronous Javascript (require.js)

Thanks to Christopher Imrie's brilliant work on RequireJS for EE you can now use Theme Loader automatically with load JavaScript resources automatically (and asynchronously) using require.js. If the RequireJS for EE extension is installed, Theme Loader will automatically use those resources to load the files - otherwise the scripts are loaded normally.

[https://github.com/ckimrie/RequireJS-for-EE](https://github.com/ckimrie/RequireJS-for-EE)

---

### How to Use

Theme Loader is very easy to use. Simple instantiate the Theme Loader class by passing the module name in the constructor. This allows Theme Builder to properly build the correct location of the file paths and URL.


	$this->EE->load->library('theme_loader', array(
		'module_name' => 'postmaster' // Your module name goes here
	));

If the Theme Loader object is already instantiated, you can update the module name like so:

	$this->EE->theme_loader->module_name = 'postmaster';
	
*The module_name should be the value of your module directory. So all lowercase is recommended.*

---

### Methods

#### css($file)

Add a CSS file to the document head.

	#this->EE->theme_loader->css('postmaster');

#### js($file)

	#this->EE->theme_loader->js('postmaster');

#### theme_url()
	
Returns a valid url to the add-on's theme folder
	
	$this->EE->theme_load->theme_url();
	
#### theme_path()
	
Returns a valid file path to the add-on theme files

	$this->EE->theme_load->theme_path();

---

### License

GNU GENERAL PUBLIC LICENSE - Refer to license.txt for details.