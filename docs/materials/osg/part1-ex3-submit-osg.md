---
status: testing
---

# OSG Exercise 3: Running Jobs in OSG

The goal of this exercise is for you to run jobs in OSG,
specifically the Open Science Pool,
and map their geographical locations.

## Where in the world are my jobs? (Part 2)

In this version of the geolocating exercise,
you will submit jobs to the OS Pool from `login04.osgconnect.net`
and hopefully get back interesting results!
You will use the same job (software) as you did in [OSG exercise 1.1](part1-ex1-submit-refresher.md).

### Gathering network information from the OSG

As a preliminary step, you will create a submit file that will run in the OS Pool!

1.  If not already logged in, `ssh` into `login04.osgconnect.net`

1.  Set the default project associated with your account by running the following command:

        :::console
        connect project

    If you are given a choice and do not know which project to select, reach out to OSG staff.
    The default project will stay in effect until changed at a later time.

1.  Make a new directory for this exercise, `osg-ex3` and change into it

1.  Copy files from `learn` (if not done already)

    Use `scp` or `rsync` from [OSG exercise 1.2](part1-ex2-login-scp.md) to copy the executable and input
    file from the `osg-ex1` directory from `learn`;
    or, if you copied the OSG exercise 1.1 tarball earlier, extract the files from it.

1.  Copy or re-create the submit file from OSG exercise 1.1,
    except this time around change your submit file so that it submits
    **five hundred** jobs!

    Do you think you should test a smaller number of jobs first and scale up?

1.  Submit your file and wait for the results

## Mapping your jobs

As before, you will be using <https://www.mapcustomizer.com/> to visualize where your jobs have landed in the OSG.
Copy and paste the collated results from your job output into the Bulk Entry area.
Where did your jobs end up?

## Next exercise

Once completed, move onto the next exercise: [Hardware Differences in the OSG](part1-ex4-hardware-diffs.md)

## Extra Challenge: Cleaning up your submit directory

If you run `ls` in the directory from which you submitted your job, you may see that you now have thousands of files!
Proper data management starts to become a requirement as you start to develop truly HTC workflows;
it may be helpful to separate your submit files, code, and input data from your output data.

1.  Try editing your submit file so that all your output and error files are saved to separate directories within your
    submit directory.

    !!! note "Tip"
        Experiment with fewer job submissions until you’re confident you have it right,
        then go back to submitting 500 jobs.
        Remember: Test small and scale up!

1.  Submit your file and track the status of your jobs.

Did your jobs complete successfully with output and error files saved in separate directories?
If not, can you find any useful information in the job logs or hold messages?
If you get stuck, review the [slides from Tuesday](../index.md).
