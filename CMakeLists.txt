cmake_minimum_required(VERSION 3.0.2)
project(common_ground_ontology)

find_package(catkin REQUIRED)

catkin_package()

include_directories()

install(DIRECTORY meshes/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/meshes
)

install(DIRECTORY textures/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/textures
)

install(FILES
  CG_actions.owl
  CG_agents.owl
  CG_area.owl
  CG_building.owl
  CG_context.owl
  CG_entities.owl
  CG_env_interaction.owl
  CG_geometric.owl
  CG_language.owl
  CG_objects.owl
  CG_root.owl
  CG_sensors.owl
  CG_verbs.owl
  ris_agents.owl
  CG_restaurant.owl
  CG_dishes.owl
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)