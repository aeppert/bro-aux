
cmake_minimum_required(VERSION 2.8)

include(RequireCXX11)

project(Plugin)

include(BroPlugin)

bro_plugin_begin(@PLUGIN_NAMESPACE@ @PLUGIN_NAME@)
bro_plugin_cc(src/Plugin.cc)
bro_plugin_bif(src/@PLUGIN_NAME_LOWER@.bif)
bro_plugin_dist_files(README CHANGES COPYING VERSION)
bro_plugin_end()
