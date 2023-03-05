# How to use it Examples
* ref: (All MicroService to Build Image)
* repo_branch : (Based on build)


# For Development
      - name: CleanUp Development old Builds
        uses: ./cleanup-source
        with:
          repo: (Based on build)
          github_token:  ${{ secrets.ACCESS_TOKEN }}
          days: Enter days
          

# For Production
      - name: CleanUp Production old Builds
        uses: ./cleanup-source
        with:
          repo: (Based on build)
          github_token:  ${{ secrets.ACCESS_TOKEN }}
          days: Enter days
          
          

# For Cleanup DevOps Maintenance
      - name: Clanup DevOps Maintenance
        uses: ./cleanup-source
        with:
          repo: (Based on build)
          github_token:  ${{ secrets.ACCESS_TOKEN }}
          days: Enter days
                    
                 
