<?php
/***
*** @CPT - Custom post type
***/

function prefix_register_all() {
	register_taxonomy(
		'type',
		array(
			'post',
		),
		array(
			'labels'            => array(
				'name'              => _x('Types', 'post', 'type_of_post'),
				'singular_name'     => _x('Type', 'post', 'type_of_post'),
				'menu_name'         => __('Type', 'type_of_post'),
				'all_items'         => __('All Type', 'type_of_post'),
				'edit_item'         => __('Edit Type', 'type_of_post'),
				'view_item'         => __('View Type', 'type_of_post'),
				'update_item'       => __('Update Type', 'type_of_post'),
				'add_new_item'      => __('Add New Type', 'type_of_post'),
				'new_item_name'     => __('New Type Name', 'type_of_post'),
				'parent_item'       => __('Parent Type', 'type_of_post'),
				'parent_item_colon' => __('Parent Type:', 'type_of_post'),
				'search_items'      => __('Search Type', 'type_of_post'),
			),
			'show_admin_column' => true,
			'hierarchical'      => true,
			'rewrite'           => array(
				'slug' => 'type'
			)
		)
	);
}
add_action('init', 'prefix_register_all', 0);
?>
