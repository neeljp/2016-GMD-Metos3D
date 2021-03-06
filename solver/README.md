#### Spin-up and Newton-Krylov solver

Setup PETSc environment:

	$> . petsc-3.3-p4.env.txt

Compile model and run experiment (submit job):

- ``MITgcm-PO4-DOP`` model:

		$> cd MITgcm-PO4-DOP/
		$> metos3d simpack MITgcm-PO4-DOP
		$> qsub job/newton.MITgcm-PO4-DOP.job
		$> qsub job/spinup.MITgcm-PO4-DOP.job
	
- ``N`` model:

		$> cd N/
		$> metos3d simpack N
		$> qsub job/newton.N.job
		$> qsub job/spinup.N.job

...

- ``NPZD-DOP`` model:

		$> cd NPZD-DOP/
		$> metos3d simpack NPZD-DOP
		$> qsub job/newton.NPZD-DOP.job
		$> qsub job/sinpup.NPZD-DOP.job

Create figures:

- ``MITgcm-PO4-DOP`` model:

		$> ./create-figures.py MITgcm-PO4-DOP/

- ``N`` model:

		$> ./create-figures.py N/

...

- ``NPZD-DOP`` model:

		$> ./create-figures.py NPZD-DOP/
