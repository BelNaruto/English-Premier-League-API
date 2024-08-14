# English Premier League API Documentation

## Overview
This API provides a variety of endpoints for retrieving data related to the English Premier League, including game box scores, summaries, schedules, standings, team information, player statistics, and more. Below is a detailed description of each endpoint, including the required parameters and the responses you can expect.
This API can be found on [RapidApi](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/english-premiere-league1)

## Endpoints

### 1. Box Score
- **Endpoint**: `/boxscore`
- **Method**: `GET`
- **Description**: Retrieves the box score for a specific game.
- **Query Parameters**:
  - `gameId` (required): The unique identifier for the game.
- **Responses**:
  - `200 OK`: Returns the box score data.
  - `400 Bad Request`: If `gameId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 2. Game Summary
- **Endpoint**: `/summary`
- **Method**: `GET`
- **Description**: Retrieves the summary for a specific game.
- **Query Parameters**:
  - `gameId` (required): The unique identifier for the game.
- **Responses**:
  - `200 OK`: Returns the game summary data.
  - `400 Bad Request`: If `gameId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 3. Schedule
- **Endpoint**: `/schedule`
- **Method**: `GET`
- **Description**: Retrieves the schedule for a specific date.
- **Query Parameters**:
  - `year` (required): The year of the schedule.
  - `month` (optional): The month of the schedule.
  - `day` (optional): The day of the schedule.
- **Responses**:
  - `200 OK`: Returns the schedule data.
  - `400 Bad Request`: If `year` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.
- **Note**: If the link doesn't contain the base URL, remember that the base URL is `https://espn.com`.

### 4. Scoreboard
- **Endpoint**: `/scoreboard`
- **Method**: `GET`
- **Description**: Retrieves the scoreboard for a specific date.
- **Query Parameters**:
  - `year` (required): The year of the scoreboard.
  - `month` (optional): The month of the scoreboard.
  - `day` (optional): The day of the scoreboard.
  - `limit` (optional, default = 100): The number of results to return.
- **Responses**:
  - `200 OK`: Returns the scoreboard data.
  - `400 Bad Request`: If `year` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 5. Standings
- **Endpoint**: `/standings`
- **Method**: `GET`
- **Description**: Retrieves the standings for a specific year and group.
- **Query Parameters**:
  - `year` (required): The year of the standings.
  - `group` (optional, default = `league`): The group of the standings. Acceptable values are `league`, `conference`, or `division`.
- **Responses**:
  - `200 OK`: Returns the standings data.
  - `400 Bad Request`: If `year` is not provided, or `group` is invalid.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 6. Team List
- **Endpoint**: `/team/list`
- **Method**: `GET`
- **Description**: Retrieves a list of teams.
- **Query Parameters**:
  - `limit` (optional, default = 400): The number of teams to return.
- **Responses**:
  - `200 OK`: Returns the list of teams.
  - `500 Internal Server Error`: If an error occurs.

### 7. Team Info
- **Endpoint**: `/team/info`
- **Method**: `GET`
- **Description**: Retrieves information about a specific team.
- **Query Parameters**:
  - `teamId` (required): The unique identifier for the team.
- **Responses**:
  - `200 OK`: Returns the team information.
  - `400 Bad Request`: If `teamId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 8. Team Roster
- **Endpoint**: `/team/roster`
- **Method**: `GET`
- **Description**: Retrieves the roster of a specific team.
- **Query Parameters**:
  - `teamId` (required): The unique identifier for the team.
- **Responses**:
  - `200 OK`: Returns the team roster.
  - `400 Bad Request`: If `teamId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 9. News
- **Endpoint**: `/news`
- **Method**: `GET`
- **Description**: Retrieves the latest news articles.
- **Query Parameters**:
  - `limit` (optional, default = 23): The number of news articles to return.
- **Responses**:
  - `200 OK`: Returns the news articles.
  - `500 Internal Server Error`: If an error occurs.

### 10. Player Season
- **Endpoint**: `/player/season`
- **Method**: `GET`
- **Description**: Retrieves the season statistics for a specific player.
- **Query Parameters**:
  - `playerId` (required): The unique identifier for the player.
  - `page` (optional, default = 1): The page of results to return.
- **Responses**:
  - `200 OK`: Returns the player's season statistics.
  - `400 Bad Request`: If `playerId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 11. Player Leagues
- **Endpoint**: `/player/leagues`
- **Method**: `GET`
- **Description**: Retrieves the leagues that a specific player has participated in.
- **Query Parameters**:
  - `playerId` (required): The unique identifier for the player.
  - `page` (optional, default = 1): The page of results to return.
- **Responses**:
  - `200 OK`: Returns the player's leagues.
  - `400 Bad Request`: If `playerId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 12. Player Statistic
- **Endpoint**: `/player/statistic`
- **Method**: `GET`
- **Description**: Retrieves statistics for a specific player.
- **Query Parameters**:
  - `playerId` (required): The unique identifier for the player.
- **Responses**:
  - `200 OK`: Returns the player's statistics.
  - `400 Bad Request`: If `playerId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 13. Team Discipline Statistics
- **Endpoint**: `/team/statistic/discipline`
- **Method**: `GET`
- **Description**: Retrieves disciplinary statistics for a specific team and season.
- **Query Parameters**:
  - `teamId` (required): The unique identifier for the team.
  - `season` (required, default = 2023): The season to retrieve data for.
- **Responses**:
  - `200 OK`: Returns the team's disciplinary statistics.
  - `400 Bad Request`: If `teamId` or `season` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 14. Team Scoring Statistics
- **Endpoint**: `/team/statistic/scoring`
- **Method**: `GET`
- **Description**: Retrieves scoring statistics for a specific team and season.
- **Query Parameters**:
  - `teamId` (required): The unique identifier for the team.
  - `season` (required, default = 2023): The season to retrieve data for.
- **Responses**:
  - `200 OK`: Returns the team's scoring statistics.
  - `400 Bad Request`: If `teamId` or `season` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 15. Team Performance
- **Endpoint**: `/team/perfomance`
- **Method**: `GET`
- **Description**: Retrieves performance data for a specific team.
- **Query Parameters**:
  - `teamId` (required): The unique identifier for the team.
- **Responses**:
  - `200 OK`: Returns the team's performance data.
  - `400 Bad Request`: If `teamId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 16. Team Transfers
- **Endpoint**: `/team/transfers`
- **Method**: `GET`
- **Description**: Retrieves transfer data for a specific team and season.
- **Query Parameters**:
  - `teamId` (required): The unique identifier for the team.
  - `season` (required, default = 2023): The season to retrieve data for.
  - `limit` (optional, default = 100): The number of transfers to return.
  - `page` (optional, default = 1): The page of results to return.
- **Responses**:
  - `200 OK`: Returns the team's transfer data.
  - `400 Bad Request`: If `teamId` or `season` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.

### 17. Get League Tables
- **Endpoint**: `/tables`
- **Method**: `GET`
- **Description**: Retrieves the league tables for a specific season.
- **Query Parameters**:
  - `season` (optional, default = `2023`): The season for which to retrieve the league tables.
- **Responses**:
  - `200 OK`: Returns the league tables data.
  - `400 Bad Request`: If `season` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.
- **Cache Behavior**: If data is available in cache, it will be served from there.

### 18. Get Injuries for the Current Season
- **Endpoint**: `/injuries`
- **Method**: `GET`
- **Description**: Retrieves a list of injuries for the current season.
- **Responses**:
  - `200 OK`: Returns the list of injuries.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.
- **Cache Behavior**: If data is available in cache, it will be served from there.

### 19. Get Team Results
- **Endpoint**: `/team/results`
- **Method**: `GET`
- **Description**: Retrieves the results for a specific team and season.
- **Query Parameters**:
  - `teamId` (required): The unique identifier for the team.
  - `season` (optional, default = `2019`): The season for which to retrieve the results.
- **Responses**:
  - `200 OK`: Returns the team results data.
  - `400 Bad Request`: If `teamId` or `season` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.
- **Cache Behavior**: If data is available in cache, it will be served from there.

### 20. Get Player Overview
- **Endpoint**: `/player/overview`
- **Method**: `GET`
- **Description**: Retrieves an overview of a specific player.
- **Query Parameters**:
  - `playerId` (required): The unique identifier for the player.
- **Responses**:
  - `200 OK`: Returns the player overview data.
  - `400 Bad Request`: If `playerId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.
- **Cache Behavior**: If data is available in cache, it will be served from there.

### 21. Get Player Statistics
- **Endpoint**: `/player/statistic`
- **Method**: `GET`
- **Description**: Retrieves the statistics for a specific player.
- **Query Parameters**:
  - `playerId` (required): The unique identifier for the player.
- **Responses**:
  - `200 OK`: Returns the player statistics data.
  - `400 Bad Request`: If `playerId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.
- **Cache Behavior**: If data is available in cache, it will be served from there.

### 22. Get Player Bio
- **Endpoint**: `/player/bio`
- **Method**: `GET`
- **Description**: Retrieves the biography of a specific player.
- **Query Parameters**:
  - `playerId` (required): The unique identifier for the player.
- **Responses**:
  - `200 OK`: Returns the player bio data.
  - `400 Bad Request`: If `playerId` is not provided.
  - `500 Internal Server Error`: If an error occurs or the parameters are incorrect.
- **Cache Behavior**: If data is available in cache, it will be served from there.

## Response Codes
- **200 OK**: Successful request, data returned in response.
- **400 Bad Request**: Missing or invalid parameters.
- **500 Internal Server Error**: An error occurred processing the request.

## Notes
- All date and time-related queries should be in the format `YYYY-MM-DD`.
- All responses will be in JSON format.
- Ensure that the parameters provided in the request are valid and in the correct format to avoid errors.
