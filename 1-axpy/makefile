# gpu architecture
sm=80
GENCODE_SM   = -gencode arch=compute_$(sm),code=sm_$(sm)
GENCODE_COMP = -gencode arch=compute_$(sm),code=compute_$(sm)

LDLIBS = -lcublas

all:
	nvcc ${GENCODE_SM} ${GENCODE_COMP} axpy.cu -o axpy ${LDLIBS}

clean:
	del /q axpy.exe axpy.lib axpy.exp