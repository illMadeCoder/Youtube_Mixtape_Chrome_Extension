# Major Terms
- playlist: A Youtube playlist.
- playlist Id: A string of characters that follows a youtube playlist URL after the '&List=' parameter.
- stage: The list of playlists a user intends to submit to be sorted.
- YTPL Sorted: An algorithm implemented 
- YTPL Sorted Endpoint: An endpoint which accepts a list of playlistIds (the stage), and a set of modulators which effect the sorted.
- Sorted Playlist: the playlist generated by the YTPL Sorted algorithm

# Pre-Alpha
- [x] Utilize Chrome Storage Sync System to save playlists on chrome user account's cloud storage
- [x] Display 'popup' window on extension icon click
- [x] Integrate React Framework
- [x] Implement Append stage button 
    - [x] look at the current tab's url for a playlist ID and append it to the user's stage
    - [x] do not append a playlist that has already been appended (no duplicate playlist ids in the stage)
    - [ ] highlight append button while on a new playlist
- [x] Implement Submit stage button
    - [x] call the local (not on the web yet) API 'YTPL Sorted Enpoint' with the stage and redirect the result to a new tab
    - [x] this stage should be stored in the user's account as StageHistory
- [x] Implement Reset stage button
        set the stage to an empty list
- [x] Display the stage
    - [x] for now a list of playlist IDs are fine
    - [x] display a button to remove the playlist from the stage
    - [ ] when the stage is empty display a message
- [x] Implement some aesthetic with a UI/UX Framework (Material UI)
- [ ] Publish to the web for friends/family usage
- [ ] Determine when/if to ever work at the video level???
    - [ ] delete videos from a playlist before the sorted playlist generates
- [x] Come up with a name (I did! 'Youtube Mixtape')    
- [ ] Endpoint should be called once per update at most
- [ ] Cache stage info so there doesn't need to be a fetch unless an update occurs
- [X] merge stage and stage info, it's unnecessary work to maintain both

# Alpha
- [ ] Display a list of some of the Previous stages    
    - [ ] On Previous Playlist Selection a UI/UX that displays the set of subplaylists to choose from that aren't already in the current stage
    - [ ] display all
- [ ] Display each staged playlist's metrics
    - [ ] views, 
    - [ ] video count, 
    - [ ] icon,
    - [ ] run length
- [ ] Detect when the user is on a playlist tab even when the extension is not open and display a popup to append the playlist
    - [ ] automatically close after x time
    - [ ] provide a disable button in options???
- [ ] Error Messages
    - [ ] append a playlist that's already in the playlist stage    
- [ ] When submitting the stage provide a menu for modulating the submission
    - [ ] Modulators:
        - [ ] Mixin: Boolean
        - [ ] SortBy: Views | Likes | Ratio | Custom | Random
        - [ ] VideosPerPlaylist: Number & Number
    - [ ] Send the modulators to the YTPL Sorted Endpoint
- [ ] Button to Star a Submitted Stage to be favorited 
    - [ ] star (favorite) button
    - [ ] a dialogue popup to name the favorited stage
    - [ ] button on click will store the stage in user storage as FavoritePlaylistStages    
    - [ ] Display list of favorited stages
        - [ ] Rename a favorited stage button 
        - [ ] Delete a favorited stage button
        - [ ] Pull in subplaylists to current stage feature implemented for previous playlists
    - [ ] Edit favorited stages
- [ ] Thank you for installing instructions page    
# Beta
- [ ] Add friends (maybe just through google chrome accounts???)
- [ ] View friend's playlists
    - [ ] public/private playlists
    - [ ] requires DB    
- [ ] Search Bar
    - [ ] fuzzy search 
    - [ ] stages        
        - [ ] favorited stages by name
        - [ ] friends favorited stages by name
    - [ ] playlists
        - [ ] playlists of previous stages
        - [ ] playlists of friends previous stages
    - [ ] song names???
    - [ ] online???
- [ ] Detect that the user is on a search result web page with a playlist as a result
    - [ ] Display a dropdown popup of all the playlists on the page
        - [ ] Display each playlist's metrics
            - [ ] views, 
            - [ ] video count, 
            - [ ] icon,
            - [ ] run length
        - [ ] On each playlist display a button to add it to the stage
            - [ ] Once a playlist has been added to a stage replace the add button with a unstage button
- [ ] Bottom arrow to go back to the top of the extension???     
- [ ] Save Sorted Playlists to the User's Channel       
# Gold  