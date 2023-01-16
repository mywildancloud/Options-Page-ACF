# Options-Page-ACF
add menu options page for ACF

> copy this code snippet below and paste

//* register a top-level options page *//
if ( function_exists( 'acf_add_options_page' ) ) {
	acf_add_options_page( [
		'page_title' => 'Themes Editor',
		'menu_title' => 'Themes Editor',
		'menu_slug' => 'themes-editor',
		'capability' => 'edit_posts',
		'parent_slug' => '',
		'position' => 5,
		'icon_url' => 'dashicons-screenoptions',
		'redirect' => true,
		'post_id' => 'options',
		'autoload' => false,
		'update_button' => 'Update',
	] );
	
	acf_add_options_sub_page(array(
        'page_title'    => 'Header',
        'menu_title'    => 'Header',
        'parent_slug'   => 'themes-editor',
    ));
    
    acf_add_options_sub_page(array(
        'page_title'    => 'Testimonials',
        'menu_title'    => 'Testimonials',
        'parent_slug'   => 'themes-editor',
    ));
	
    acf_add_options_sub_page(array(
        'page_title'    => 'Footer',
        'menu_title'    => 'Footer',
        'parent_slug'   => 'themes-editor',
    ));

}
