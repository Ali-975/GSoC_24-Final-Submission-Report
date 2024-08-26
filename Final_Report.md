# Final Report

**Student**: Muddassir Ali  
**Mentor**: [Mehdi Saligane](https://github.com/msaligane)  
**Project**: [GDS Reader/Writer Implementation in OpenROAD](https://github.com/chipsalliance/ideas/blob/main/gsoc-2024-ideas.md#create-a-gds-readerwriter-in-openroad)  
**Organization**: [Chips Alliance](https://github.com/chipsalliance)

---

## Project Description

**Create a GDS Reader/Writer in OpenROAD**

The GDS (Graphic Design Stream) format is crucial for creating visual representations of physical layouts in OpenROAD. Currently, OpenROAD relies on a workaround involving klayout to read and write GDS files, which is neither efficient nor ideal. The aim of this project was to directly implement GDS read and write functionality within OpenROAD using OpenDB (ODB), eliminating the need for external tools and providing a more integrated solution.

## Task Description

1. **Familiarization**:  
   - Studied the OpenROAD documentation and source code.
   - Analyzed the LEF and DEF classes, which already had reader and writer implementations, to understand their structure.

2. **GDS-II Format Understanding**:  
   - Gained in-depth knowledge of the GDS-II format, essential for implementing the reader and writer classes.

3. **Implementation**:  
   - Successfully implemented `gdsin` and `gdsout` classes within OpenROAD, leveraging OpenDB to handle GDS data natively.

4. **Collaboration and Review**:  
   - Engaged with OpenROAD community members, discussing and reviewing the feature PR to ensure alignment with the project's goals and standards.
   - [History of GSoC merge and pull requests](https://github.com/The-OpenROAD-Project/OpenROAD/compare/master...Ali-975:OpenROAD:master).

## Expected Outcomes

The main goal was to replace the current hacky methods of handling GDS files in OpenROAD with a robust, native solution. By implementing the GDS reader/writer using OpenDB, OpenROAD now has a reliable method for handling GDS files internally, improving the workflow and integration within the tool.

## Work Done

Throughout this project, the team focused on implementing the `gdsin` and `gdsout` classes, which required a deep understanding of both the OpenDB structure and the GDS-II format. These classes were designed to read and write GDS files directly within OpenROAD, eliminating the previous dependency on external tools. The integration was carefully reviewed and tested to ensure it met the project's standards and objectives.

## What’s Left to Do

The main implementation tasks have been completed. The remaining work involves:
- Comprehensive testing of the GDS reader/writer to ensure it handles all potential edge cases and operates reliably under various conditions.

## Acknowledgments

I would like to extend my gratitude to my mentor, [Mehdi Saligane](https://github.com/msaligane), for his invaluable guidance throughout this project. Special thanks also to [Barry Lyu](https://github.com/fangzhonglyu) and [Matt Liberty](https://github.com/maliberty), whose cooperation and support were instrumental in the successful completion of this project.

## Conclusion

This project involved the implementation of a native GDS reader/writer in OpenROAD, using OpenDB to manage GDS data. By replacing the previous workaround methods, this new functionality enhances the tool's efficiency and reliability. The experience has been enriching, offering deep insights into both software development and the collaborative nature of open-source communities.
