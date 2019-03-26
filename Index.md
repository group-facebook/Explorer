<H2> WELCOME TO GROUP FACEBOOK</>
<br>
<a id="for html" a href="https://travis-ci.org/on-store/Marketplace-Store"><img src="https://travis-ci.org/on-store/Marketplace-Store.svg?branch=master"></a>
</br>
<br>

<title>Apps-script/snippets/apps-script.gs</title>
<a Id="Apps-script" a href="Sample Apps Script code for printing API response data
function printResults(response) {
  var props = ['type', 'title', 'textDisplay', 'channelId', 'videoId', 'hl', 'gl', 'label'];
  for (var r = 0; r < response['items'].length; r++) {
    var item = response['items'][r];
    var itemId = '';
    var value;
    if (item['rating']) {
      itemId = item['id'];
      value = 'Rating: ' + item['rating'];
    } else {
      if (item['id']['videoId']) {
        itemId = item['id']['videoId'];
      } else if (item['id']['channelId']) {
        itemId = item['id']['channelId'];
      } else {
        itemId = item['id'];
      }
      
      for (var p = 0; p < props.length; p++) {
        if (item['snippet'][props[p]]) {
          value = itemId + ': ' + item['snippet'][props[p]];
          break;
        }
      }
    }
    Logger.log(value);
  }
}

/**
 * This example retrieves the 25 most recent activities for the Google Developers 
 * channel. It retrieves the snippet and contentDetails parts for each activity 
 * resource. 
 */
function activitiesList(part, channelId, maxResults) {
  var response = YouTube.Activities.list(part,
      {'channelId': channelId,
       'maxResults': maxResults});
  printResults(response);
}

/**
 * This example retrieves the 25 most recent activities performed by the user 
 * authorizing the API request. 
 */
function activitiesListMine(part, maxResults, mine) {
  var response = YouTube.Activities.list(part,
      {'maxResults': maxResults,
       'mine': mine});
  printResults(response);
}

/**
 * This example lists caption tracks available for the Volvo Trucks "Epic Split" 
 * commercial, featuring Jean-Claude Van Damme. (This video was selected because 
 * it has many available caption tracks and also because it is awesome.) 
 */
function captionsList(part, videoId) {
  var response = YouTube.Captions.list(part, videoId);
  printResults(response);
}

/**
 * This example retrieves channel data for the GoogleDevelopers YouTube channel. 
 * It uses the id request parameter to identify the channel by its YouTube channel 
 * ID. 
 */
function channelsListById(part, id) {
  var response = YouTube.Channels.list(part,
      {'id': id});
  printResults(response);
}

/**
 * This example retrieves channel data for the GoogleDevelopers YouTube channel. 
 * It uses the forUsername request parameter to identify the channel by its 
 * YouTube username. 
 */
function channelsListByUsername(part, forUsername) {
  var response = YouTube.Channels.list(part,
      {'forUsername': forUsername});
  printResults(response);
}

/**
 * This example retrieves the channel data for the authorized user's YouTube 
 * channel. It uses the mine request parameter to indicate that the API should 
 * only return channels owned by the user authorizing the request. 
 */
function channelsListMine(part, mine) {
  var response = YouTube.Channels.list(part,
      {'mine': mine});
  printResults(response);
}

/**
 * This example retrieves the channel sections shown on the Google Developers 
 * channel, using the channelId request parameter to identify the channel. 
 */
function channelSectionsListById(part, channelId) {
  var response = YouTube.ChannelSections.list(part,
      {'channelId': channelId});
  printResults(response);
}

/**
 * This example retrieves the channel sections shown on the authorized user's 
 * channel. It uses the mine request parameter to indicate that the API should 
 * return channel sections on that channel. 
 */
function channelSectionsListMine(part, mine) {
  var response = YouTube.ChannelSections.list(part,
      {'mine': mine});
  printResults(response);
}

/**
 * This example retrieves comment replies for a specified comment, which is 
 * identified by the parentId request parameter. In this example, the parent 
 * comment is the first comment on a video about Apps Script. The video was chosen 
 * because this particular comment had multiple replies (in multiple languages) 
 * and also because Apps Script is really useful. 
 */
function commentsList(part,"</a>
