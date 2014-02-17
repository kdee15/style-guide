style-guide
===========

Front end code style guide I generally use.

# File Structure Guidelines

Keep file structures in a consistent pattern for each project, allows all of us to just dive into a project and work. This is the current suggested pattern:

1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
 

- - -

# Commenting Guidelines

Commenting code in a consistent and uniform manner is vital to working as a team. It allows everyone to expect a certain pattern, meaning they can navigate and find certain items quickly.

Following the pattern is half the battle. Useful, descriptive comments make up the other half. We need to know exactly what each section / component does, and whether there are any things we need to take note of.

Sectioning of segments of code makes it easy to read through code in a predictable manner. Always opt for more comments. We can always strip them out with Grunt.js on production sites. 

## HTML

## Javascript

## CSS

We use SCSS (SASS) as our CSS pre-processor, therefore we implement comments using the SASS comment format. This will strip out the comments on processing, giving us a cleaner output CSS.

    // A. BIG SECTION LIKE A PAGE OR A FEATURE (ex: MAST) ++++++++++++++++++++++++++++++++++++
    
        #masthead {
    
        // A.1. MAJOR COMPONENT WITHING SECTION (ex: SIDEBAR)
        
            .sidebar {
            
                // A.1.1. Minor component
                
                // NOTE: This block is overridden from the default reusable pattern at [B.1.1. Generic Block]. 
                
                .aside-block {}
                
                // A.1.1. End
            
            }
        
        // A.1. END
        
        }
    
    // A. END ++++++++++++++++++++++++++++++++++++

- - -
