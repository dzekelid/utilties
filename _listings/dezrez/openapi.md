---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/role/lettings/{id}/saveutility:
    post:
      summary: Add or Update a utility for the letting role
      description: Add or update a utility for the letting role.
      operationId: LettingRole_SaveUtilityByidBysaveUtilityDataContract
      x-api-path-slug: apirolelettingsidsaveutility-post
      parameters:
      - in: path
        name: id
        description: The letting role id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: saveUtilityDataContract
        description: The details of the utility to be added
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Utilitythe
      - Letting
      - Role
  /api/role/lettings/{roleId}/removeutility:
    delete:
      summary: Remove a utility for the letting role
      description: Remove a utility for the letting role.
      operationId: LettingRole_RemoveUtilityUtilityByroleIdByutilityId
      x-api-path-slug: apirolelettingsroleidremoveutility-delete
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
        description: The letting role Id
      - in: query
        name: utilityId
        description: The utility Id
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Utilitythe
      - Letting
      - Role
---