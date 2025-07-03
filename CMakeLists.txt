cmake_minimum_required(VERSION 3.10.0)
project(common_ground_ontology)

if($ENV{ROS_VERSION} STREQUAL "1")
  find_package(catkin REQUIRED)

  catkin_package()
elseif($ENV{ROS_VERSION} STREQUAL "2")
  find_package(ament_cmake REQUIRED)
endif()


if($ENV{ROS_VERSION} STREQUAL "1")
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
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
  )

elseif($ENV{ROS_VERSION} STREQUAL "2")

  install(DIRECTORY meshes DESTINATION share/${PROJECT_NAME}/)
  install(DIRECTORY textures DESTINATION share/${PROJECT_NAME}/)

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
    DESTINATION share/${PROJECT_NAME}/
  )

  ament_package()
endif()