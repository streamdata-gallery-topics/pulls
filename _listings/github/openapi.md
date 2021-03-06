swagger: "2.0"
x-collection-name: GitHub
x-complete: 1
info:
  title: GitHub
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repos/{owner}/{repo}/pulls:
    get:
      summary: Get Repos Owner Repo Pulls
      description: List pull requests.
      operationId: list-pull-requests
      x-api-path-slug: reposownerrepopulls-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: base
        description: Filter pulls by base branch name
      - in: query
        name: head
        description: Filter pulls by head user and branch name in the format of user:ref-name
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: state
        description: String to filter by state
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
    post:
      summary: Add Repos Owner Repo Pulls
      description: Create a pull request.
      operationId: create-a-pull-request
      x-api-path-slug: reposownerrepopulls-post
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
  /repos/{owner}/{repo}/pulls/comments:
    get:
      summary: Get Repos Owner Repo Pulls Comments
      description: |-
        List comments in a repository.
        By default, Review Comments are ordered by ascending ID.
      operationId: list-comments-in-a-repositoryby-default-review-comments-are-ordered-by-ascending-id
      x-api-path-slug: reposownerrepopullscomments-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
        description: Ignored without sort parameter
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: since
        description: 'The time should be passed in as UTC in the ISO 8601 format:
          YYYY-MM-DDTHH:MM:SSZ'
      - in: query
        name: sort
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Comments
  /repos/{owner}/{repo}/pulls/comments/{commentId}:
    delete:
      summary: Delete Repos Owner Repo Pulls Comments Comment
      description: Delete a comment.
      operationId: delete-a-comment
      x-api-path-slug: reposownerrepopullscommentscommentid-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: Id of comment
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Comments
      - Comment
    get:
      summary: Get Repos Owner Repo Pulls Comments Comment
      description: Get a single comment.
      operationId: get-a-single-comment
      x-api-path-slug: reposownerrepopullscommentscommentid-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: commentId
        description: Id of comment
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Comments
      - Comment
    patch:
      summary: Patch Repos Owner Repo Pulls Comments Comment
      description: Edit a comment.
      operationId: edit-a-comment
      x-api-path-slug: reposownerrepopullscommentscommentid-patch
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: commentId
        description: Id of comment
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Comments
      - Comment
  /repos/{owner}/{repo}/pulls/{number}:
    get:
      summary: Get Repos Owner Repo Pulls Number
      description: Get a single pull request.
      operationId: get-a-single-pull-request
      x-api-path-slug: reposownerrepopullsnumber-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
    patch:
      summary: Patch Repos Owner Repo Pulls Number
      description: Update a pull request.
      operationId: update-a-pull-request
      x-api-path-slug: reposownerrepopullsnumber-patch
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
  /repos/{owner}/{repo}/pulls/{number}/comments:
    get:
      summary: Get Repos Owner Repo Pulls Number Comments
      description: List comments on a pull request.
      operationId: list-comments-on-a-pull-request
      x-api-path-slug: reposownerrepopullsnumbercomments-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
      - Comments
    post:
      summary: Add Repos Owner Repo Pulls Number Comments
      description: |-
        Create a comment.
          #TODO Alternative input ( http://developer.github.com/v3/pulls/comments/ )
          description: |
            Alternative Input.
            Instead of passing commit_id, path, and position you can reply to an
            existing Pull Request Comment like this:

                body
                   Required string
                in_reply_to
                   Required number - Comment id to reply to.
      operationId: create-a-comment--todo-alternative-input--httpdevelopergithubcomv3pullscomments---description-----al
      x-api-path-slug: reposownerrepopullsnumbercomments-post
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
      - Comments
  /repos/{owner}/{repo}/pulls/{number}/commits:
    get:
      summary: Get Repos Owner Repo Pulls Number Commits
      description: List commits on a pull request.
      operationId: list-commits-on-a-pull-request
      x-api-path-slug: reposownerrepopullsnumbercommits-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
      - Commits
  /repos/{owner}/{repo}/pulls/{number}/files:
    get:
      summary: Get Repos Owner Repo Pulls Number Files
      description: List pull requests files.
      operationId: list-pull-requests-files
      x-api-path-slug: reposownerrepopullsnumberfiles-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
      - Files
  /repos/{owner}/{repo}/pulls/{number}/merge:
    get:
      summary: Get Repos Owner Repo Pulls Number Merge
      description: Get if a pull request has been merged.
      operationId: get-if-a-pull-request-has-been-merged
      x-api-path-slug: reposownerrepopullsnumbermerge-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
      - Merge
    put:
      summary: Put Repos Owner Repo Pulls Number Merge
      description: Merge a pull request (Merge Button's)
      operationId: merge-a-pull-request-merge-buttons
      x-api-path-slug: reposownerrepopullsnumbermerge-put
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: number
        description: Id of pull
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Pulls
      - Number
      - Merge