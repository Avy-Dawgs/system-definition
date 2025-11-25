# system-definition
Diagrams, requirements, and specifications for components and interfaces that make up the system.

## System Diagram
![](./.diagrams/system-diagram.drawio.svg)

This diagram shows the top level components of the system, divided into two different physical systems, the drone 
and the base station.

## System Description 
This system locates avalanche beacons using an autonomous drone, relaying the location of the identified 
beacons back to a base station.

## Navigating this Repository
* Requirements and specifications are listed by component in the ```components``` folder.
* Interfaces between components are described in the ```interfaces``` folder.
* Diagrams are all made in drawio and saved as svg, and can be found in the ```.diagrams``` folder.
    * Note that all diagrams are embedded in their corresponding markdown files.
